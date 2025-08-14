# recipe-app-api
Recipe API projects

# project goal
Step    1 - Create a recipe api to record the Chinese food recipe my girlfriend and I created and performed
            1.1 - use Test-Driven Development
                1.1.1 - @patch for unittest.mock
                1.1.2 - django.test
            1.2 - use docker-compose image
                1.2.1 - (app) use django REST framework
                1.2.2 - (database) use PostgreSQL
                      1.2.2.1 - packages
                              * psycopg2-binary
                                -OK for development
                                -Not good for prod
                              *psycopg2
                                -Compiles from source
                                -Required additional dependencies
                                  1. C compiler
                                  2. python3-dev
                                  3. libpq-dev
                                -Equivalent dependency packages for Alpine (clean up after built)
                                  1. postgresql-client
                                  2. build-base
                                  3. postgresql-dev
                                  4. musl-dev
                                -Easy to use in Docker
                      1.2.2.2 - define model & migration in docker-compose.yml
                1.2.3 - app1: wait_for_db
                  * deal with database race conditions