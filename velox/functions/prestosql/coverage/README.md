# Coverage Maps

Velox includes a subset of scalar and aggregate Presto functions.
velox_prestosql_coverage utility is used to generate a list of available
functions and coverage maps showing which subset of all and most used functions
is available. The output uses reStructured text format suitable for use in
Velox documenation.

> velox_prestosql_coverage

Generates a list of Presto functions available in Velox. The output
to be copy-pasted into velox/docs/functions.rst file.

> velox_prestosql_coverage --all

Generates coverage map using all Presto functions. The output to be copy-pasted
into velox/docs/coverage.rst file. The functions appear in alphabetical order.

The list of all scalar and aggregate Presto functions comes from
data/all_scalar_functions.txt and data/all_aggregate_functions.txt files respectively.

These files were created using output of SHOW FUNCTIONS Presto command.

> velox_prestosql_coverage --most_used

Generates coverage map using a subset of most used Presto functions. The output
to be copy-pasted into velox/docs/mostd_used_coverage.rst file. The functions
appear in order from most used to least used.

The list of most used Presto functions comes from data/most_used_functions.txt file
which contains a mix of scalar and aggregate function names in the order from
most used to least used.
