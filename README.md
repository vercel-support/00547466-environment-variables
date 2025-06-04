# Vercel System Environment Variable Test

## Purpose

This project checks whether Vercel system environment variables (like `VERCEL`) are available in different build script scenarios.

## What We’re Testing

- If `VERCEL` is available in an npm `postbuild` script.
- If `VERCEL` is available when the postbuild script is chained directly in the `build` command.

## How to Test

1. Deploy this project to Vercel.
2. Check the build logs for the output of `postbuild.js`:
   - First, with `postbuild` as an npm lifecycle script.
   - Then, by chaining it in the `build` command:  
     `"build": "next build && node postbuild.js"`

## Why

To determine the most reliable way to access Vercel system environment variables during the build process.

## References

- [Vercel: System Environment Variables](https://vercel.com/docs/environment-variables/system-environment-variables)
