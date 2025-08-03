# Homebrew Tap for CIB IB Tech SRE CLI

This is the official Homebrew tap for the CIB IB Tech SRE CLI (`cibibtsre`).

## Installation

```bash
# Add the tap
brew tap ab0350a/homebrew-cibibtsre

# Install cibibtsre
brew install cibibtsre

# Verify installation
cibibtsre --version
```

## One-liner Installation

```bash
curl -sSL https://raw.githubusercontent.com/ab0350a/homebrew-cibibtsre-cli-go/main/install-homebrew.sh | bash
```

## About

The CIB IB Tech SRE CLI is a high-performance command-line interface for AWS Control Tower BYOT (Bring Your Own Tofu) onboarding automation, rewritten in Go for dramatically improved performance.

### Performance Improvements

| Command | Python Version | Go Version | Improvement |
|---------|---------------|------------|-------------|
| `--help` | 25+ seconds | **< 50ms** | **500x faster** |
| `--version` | 20+ seconds | **< 50ms** | **400x faster** |
| `tf-onboard` | 30+ seconds | **< 5 seconds** | **6x faster** |
| `byot-quick-start` | 30+ seconds | **< 5 seconds** | **6x faster** |

## Features

- **CloudFormation Stack Auto-Discovery** - Automatically discovers team information from existing stacks
- **AWS Budgets Quick-Start** - Complete AWS Budgets infrastructure automation
- **Azure DevOps Integration** - Seamless pipeline and repository creation
- **Template-Based Generation** - Uses standardized templates for consistency
- **Cross-Platform Support** - Works on macOS, Linux, and Windows

## Usage

```bash
# Interactive onboarding
cibibtsre tf-onboard

# Generate AWS Budgets infrastructure
cibibtsre byot-quick-start aws-budgets \
  --ado-project "Your-Project" \
  --ado-repo "aws-budgets-monitoring" \
  --ado-token "your-token" \
  --github-pat "your-github-token" \
  --servicenow-ci BSN0022061 \
  --aws-account-id 123456789012 \
  --aws-region eu-west-1 \
  --environment uat \
  --create-new-repo

# Get help
cibibtsre --help
```

## Links

- **Main Repository**: https://github.com/ab0350a/homebrew-cibibtsre-cli-go
- **Documentation**: https://github.com/ab0350a/homebrew-cibibtsre-cli-go/tree/main/docs
- **Releases**: https://github.com/ab0350a/homebrew-cibibtsre-cli-go/releases

## Support

For issues, questions, or contributions, please visit the main repository at https://github.com/ab0350a/homebrew-cibibtsre-cli-go.
