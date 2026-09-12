# Maness Software Consulting website

Static marketing site for Maness Software Consulting, hosted on AWS Amplify.

## Layout

```
.
├── amplify.yml        # Amplify Hosting build spec (no build step, serves public/)
├── public/            # Everything in here is deployed as-is
│   ├── index.html
│   ├── favicon.ico
│   └── images/        # Logo SVGs
└── docs/              # Local drafts and reference material (gitignored)
```

## Local preview

```
python3 -m http.server 8000 --directory public
```

Then open http://localhost:8000.

## Deploying

Amplify Hosting is connected to the `main` branch of this repo. Every push to
`main` triggers a deploy using `amplify.yml`, which publishes the contents of
`public/` with no build step.
