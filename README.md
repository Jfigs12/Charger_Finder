Polestar 2
The Idea:
- Charging Network Finder Idea
- Continuously check where there are chargers around, Levels 2 and 3.
    - Check how many stalls are available
    - Check/pull charging speed
    - Check outages and at which chargers
    - Enable client interaction
        - Likes, Comments, Photos, 
        - Intake Car make, Model, year, Adapter, etc
            - Sort chargers by compatibility and charging speed
        - Intake card information
            - CC for starting a charge remotely 
                - Ex. ChargePoint API
        - Integrate questions every x chargers to check accuracy of charger status
Systems:
- SCM - (GitHub, Git Lab)
- Server Platform (AWS)
- CI/CD Pipeline(GitLab, Built in features in AWS)
- Docker or Something similar for Deployment
- Containerization(Kuberneties)

Different Builds Needed:
- REST API
    - Call it for basic information
        - Chargers Open at certian station
        - Usage information
        - Outage information
        - Speed of Charger
        - ETC
    - Have it running on AWS
- Server that is constantly running and updaing based off of values called from REST API
    - Have it update when server is called or every n time
    - Do Security Checks
    - Access Database

- Vault
    - Keep information such as API Keys
    - Hash information
    - ETC
- SQL Database Server
    - Multiple tables
        - User info
        - Car info
        - Social Information
        - Charger Information
    - Keep Patron information
    - Car information
    - last charge
    - Ratings of chargers
    - Posts to chargers
    - ETC

Considerations:
- Maybe use GitLab instead of GitHub instead of for Built in CI/CD integration
- AWS to host the REST API Server
- Create a SQL Database to run what we need

