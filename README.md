# Liquibase Secure — Amazon DynamoDB Integration

> 📖 **Full Documentation:** [Connect Liquibase with Amazon DynamoDB (Secure)](https://docs.liquibase.com/secure/integration-guide-5-2/connect-liquibase-with-amazon-dynamodb-secure)

---

## Prerequisites

### 1. Liquibase License Key

Ensure your Liquibase license key is set before running any commands.For example, you can use an environment variable:

```bash
export LIQUIBASE_LICENSE_KEY=<your-license-key>
```

---

### 2. DynamoDB Extension

How you install the extension depends on your Liquibase version:

| Version | What to do |
|---|---|
| **Liquibase Secure 5.0+** | ✅ AWS Extension is bundled — no action needed |
| **Liquibase 4.31.0 – 4.x** | Install the [AWS Extension (includes DynamoDB)](https://mvnrepository.com/artifact/org.liquibase.ext/liquibase-aws-extension) |
| **Liquibase < 4.31.0** | Install the [DynamoDB Extension](https://mvnrepository.com/artifact/org.liquibase.ext/liquibase-commercial-dynamodb) |

For versions below Liquibase Secure 5.0, place the downloaded `.jar` file in your `liquibase/lib` folder.

---

### 3. AWS Credentials

The following environment variables must be set to authenticate with AWS:

```bash
export AWS_ACCESS_KEY_ID=<your-access-key-id>
export AWS_SECRET_ACCESS_KEY=<your-secret-access-key>
export AWS_SESSION_TOKEN=<your-session-token>   # Optional — required for temporary credentials
```

---

### 4. Required IAM Permissions

Your AWS credentials must have the necessary DynamoDB permissions. See the full list of required permissions in the [official documentation](https://docs.liquibase.com/secure/integration-guide-5-2/connect-liquibase-with-amazon-dynamodb-secure).

---

## Quick Setup Checklist

- [ ] `LIQUIBASE_LICENSE_KEY` environment variable is set
- [ ] Correct DynamoDB/AWS extension installed for your Liquibase version
- [ ] `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY` are set
- [ ] AWS IAM permissions are configured per the documentation
