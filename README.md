# docker-murano-tests
This test-suite created for testing Docker Applications in Murano on MOX.
In future it will be used by Murano Team for testing Docker Applications in murano kilo-release.

# How to run

You need to install requirements.txt and configure config.conf.
Please remember, murano_url should ends by port, not by a version.

You can use nosetests to run tests directly.

    pip install nose

For high priority sanity test cases you need to run test_deploy_docker.py

    nosetests -sv test_deploy_docker.py

Running single test from test-suite

    nosetests -sv test_deploy_docker.py:MuranoDockerTest.test_deploy_docker_redis

For advanced test cases you need to use test_deploy_docker_advanced.py

    nosetests -sv test_deploy_docker_advanced.py

If you want to run single test from advanced cases, you need to do the same as
in sanity.

    nosetests -sv test_deploy_docker_advanced.py:MuranoDockerTestAdvanced.test_deploy_docker_mongodb_wait_deploy_nginx

