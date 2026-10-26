# SQLite OTP Authentication and Joke QR Codes

Demonstrates a notebook-based authentication flow backed by SQLite. A user receives a Google Authenticator provisioning QR code, signs in with a password and TOTP, retrieves a random joke from an API, and converts the joke to a QR image.

## Workflow

1. Create the SQLite users table.
2. Register a demonstration user and generate a TOTP secret.
3. Create a Google Authenticator provisioning QR code.
4. Validate a username, password, and one-time code.
5. Fetch a random joke and export it as a QR code.

## Data Requirements

- No external dataset is required; `users.db` is created at runtime.
- The notebook calls the Official Joke API.

Datasets and generated artifacts are not included unless they are embedded directly in the notebook.

## Requirements

- pyotp
- qrcode
- Pillow
- requests
- SQLite (Python standard library)
- IPython

Install missing packages in your Jupyter or Google Colab environment before running the notebook.

## Running the Notebook

1. Open [`LoginOTPSQLite_QRCode_API_Final.ipynb`](LoginOTPSQLite_QRCode_API_Final.ipynb) in Jupyter Notebook or Google Colab.
2. Place any required data files in the path expected by the notebook.
3. Update local or Google Drive paths where needed.
4. Run the cells from top to bottom.

## Outputs

- Runtime SQLite database
- Authenticator QR image
- Joke QR image

## Security and Responsible Use

This is an educational prototype. It stores passwords as plaintext and prints enrollment secrets, so it must not be used as a production authentication system. Public-copy outputs and personal sample values were sanitized.

## Repository Contents

```text
.
|-- README.md
`-- LoginOTPSQLite_QRCode_API_Final.ipynb
```

## Notes

- This repository preserves the analysis as a notebook-first educational project.
- Results may vary with dataset versions, random splits, package versions, and available hardware.
- Review file paths and runtime-specific commands before executing outside Google Colab.
