# github-actions-terraforn-drift-detection

This repo is reusable github action that check for any terraform drift detection, and sends notifications to Slack.

## Inputs

- `working_directory`: The directory where Terraform files are located (default: `./`)
- `slack_webhook`: Slack Webhook URL for notifications (required)
- `environment`: The environment name (e.g., `dev`, `prod`) (required)
- `aws_region`: AWS Region to use for Terraform (required)
- `aws_role`: IAM role ARN to assume for AWS credentials (required)

## Example Usage

```yaml
uses: your-username/terraform-plan-action@v1.0.0
with:
  working_directory: "./"
  slack_webhook: ${{ secrets.SLACK_WEBHOOK_URL }}
  environment: "dev"
  aws_region: "us-west-2"
  aws_role: ${{ secrets.AWS_ROLE }}
```
