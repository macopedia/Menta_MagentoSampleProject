# Menta Magento Sample Project

All test should works in demo magento 1.8 with sample data
## Getting started
    # Install magento with sample data. Default currency "US$"
    http://www.magentocommerce.com/wiki/1_-_installation_and_configuration/installing_magento_via_shell_ssh
    # Create admin, frontend and soap user.
    # Change settings in conf/defaults.xml or create a new configuration file

    git clone https://github.com/macopedia/Menta_MagentoSampleProject.git Menta_MagentoSampleProject
    cd Menta_SampleProject
    ./composer.phar install

    # Creating directory for HTML reports
    cd Tests
    mkdir -p ../build/reports

    # download selenium server - selenium-server-standalone-<version-number>.jar
    http://docs.seleniumhq.org/download/

    # run selenium server
    java -jar selenium-server-standalone-<version-number>.jar

    # run single test
    ../bin/phpunit --configuration=../conf/defaults.xml General/ScreenshotsTest.php

    # run all tests
    ../bin/phpunit --configuration=../conf/defaults.xml ../vendor/aoemedia/menta/lib/Menta/Util/CreateTestSuite.php