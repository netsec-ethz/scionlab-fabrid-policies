# FABRID Global Policies for SCIONLab

This repository contains a mapping of global policies to policy descriptions for **FABRID** in **SCIONLab**. Each policy is stored in JSON format in their own file.

## Overview
FABRID is a framework for SCION that allows AS operators to announce policies for their intra-AS paths. These policies can be thought of as additional path constraints: an end host can select a policy during path selection, which will ensure that their data packets are only forwarded over the policy-compliant intra-AS Path. An example of such a policy would be to denote a high-bandwidth intra-AS path or a low-latency intra-AS path. For more details about the design and functionality of FABRID, please refer to the [FABRID Design Document](https://github.com/netsec-ethz/scion/blob/scionlab/doc/dev/design/FABRID.rst).

## Repository Structure

Each policy is represented as a JSON file with the following format:

```json
{
    "description": "Test policy"
}
```

This policy structure may be extended in the future with arbitrary attributes.

### File Naming Convention

- Each file should be named according to their policy identifier e.g. for G1234 `1234.json`.

## Usage

### Adding a Policy
There currently is no procedure for controlling the accepted policies. This may be added in the future. 

1. Create a new JSON file in the repository following the structure mentioned above.
2. Add your desired policy description.

### Validating a Policy

Ensure that your JSON policy files are valid and conform to the expected schema. Use tools such as `jq` to validate the file structure.

```bash
jq '.' your_policy.json
```

## License

This repository is licensed under the [MIT License](LICENSE).

---
For questions or support, please open an issue.
```
