# Dienstleistungsvertrag — LaTeX-Vorlage

Reusable LaTeX template for German freelance service contracts (Dienstleistungsvertrag) tailored to IT consulting and software development.

## Features

- All client-specific data parameterized via `\newcommand` variables at the top
- Unfilled fields highlighted in yellow in the compiled PDF
- Scheinselbständigkeit protection clauses (§5.9–5.11)
- IP transfer / licensing (§6)
- Confidentiality with contractual penalty (§7)
- Appendix (Anlage 1) with customizable scope of services

## Usage

1. Copy `Dienstleistungsvertrag-Vorlage.tex`
2. Fill in the variables at the top of the file (everything between the `═══` lines)
3. Customize Anlage 1 (scope of services) for your client
4. Compile with XeLaTeX:

```bash
xelatex Dienstleistungsvertrag-Vorlage.tex
xelatex Dienstleistungsvertrag-Vorlage.tex  # second pass for page refs
```

## Variables

| Variable | Description | Example |
|---|---|---|
| `\ClientName` | Full company name + address | `ACME GmbH, Musterstr. 1, 10115 Berlin` |
| `\ClientKurzname` | Short name for body text | `ACME` |
| `\ClientAdresse` | Company address | `Musterstr. 1, 10115 Berlin` |
| `\ClientStadt` | City (for signature block) | `Berlin` |
| `\ClientBeschreibung` | One sentence about the client's business | `ACME betreibt eine SaaS-Plattform für...` |
| `\Vertragsbeginn` | Contract start date | `01.01.2027` |
| `\Mindestlaufzeit` | Minimum term (months) | `6` |
| `\Stundensatz` | Hourly rate (net, EUR) | `120,00` |
| `\Mindeststunden` | Monthly minimum hours | `80` |
| `\Monatsverguetung` | Monthly minimum payment (net) | `9.600,00` |
| `\RolloverCap` | Max rollover hours | `40` |
| `\Vertragsstrafe` | Confidentiality penalty (EUR) | `5.000,00` |

## Requirements

- XeLaTeX (TeX Live 2024+)
- Helvetica font (or change `\setmainfont{}`)

## Disclaimer

This template is provided as-is for informational purposes. It is not legal advice. Have your contract reviewed by a qualified attorney before use.

## License

MIT
