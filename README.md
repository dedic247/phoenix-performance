Sample instructions:

	# Build data. This sample is for a small sandbox.
	./generate_data.sh 2 && \
		./load_data.sh 2 sandbox.hortonworks.com:2181:/hbase-unsecure

	# Edit testhosts to specify the hosts that will run JMeter.
	# Assumes passwordless SSH access.

	# Setup the test environment.
	./build_driver.sh && \
		./setup_testenv.sh

	# Switch into the directory for running tests
	cd runner
	# Run various styles of queries providing the JMX "scenario"
	./RunPointStyle.sh ../jmeter_tests/Point_NoJoin_NoGroup_Pri1.jmx
