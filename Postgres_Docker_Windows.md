## Create and run Postgres in a Docker container on Windows

0. Install Docker for Windows
1. run in cmd docker "docker pull postgres" to get the latest docker image
2. run in cmd docker run --rm -e POSTGRES_PASSWORD=chooseOwnPassword --name pg_test -P postgres
3. go to cli of running postgres docker container with name pg_test
4. in cli enter "su - postgres"
5. in cli enter "create user testuser" to create the user with name testuser
6. in cli enter "createdb testdb" to create the the db with name testdb
7. in cli enter "psql" to access postgres shell
8. in postgres shell enter "alter user testuser with encrypted password 'qwerty';" to set the password for testuser
9. in postgres shell enter "grant all privileges on database testdb to testuser" to grant testuser all rights for testdb
10. connect to db via dBeaver or LinqPad or what else. Connectionstring if hosted locally: Host=localhost;Port=5432;Database=testdb;User ID=testuser;Password=qwerty
