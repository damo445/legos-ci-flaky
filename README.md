# legos-ci

Small Python test suite used to produce CI history for connector evaluation.

Most tests pass. Three do not behave:

- `test_checkout_session_timeout` fails when the CircleCI build number is even
- `test_payment_retry_on_gateway_503` fails when the build number is divisible by three
- `test_legacy_tax_rule_pre_2020` fails on every run

Run locally with `pytest`. Set `CIRCLE_BUILD_NUM` to simulate a given build.
