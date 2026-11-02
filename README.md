# 196969.github.io

Host-root robots policy for this GitHub account.

## What this repository is

One file: `robots.txt`, served at `https://196969.github.io/robots.txt`.

Crawlers read robots.txt **only at the host root**. A `robots.txt` committed
inside a project repository is served at
`https://196969.github.io/<repo>/robots.txt`, which no crawler reads — it is
inert on its own. This repository is the one that acts.

## Setup

1. Repository name must be exactly `196969.github.io`. Any other name does
   not serve at the host root, and the file goes back to being inert.
2. Public. A private repository does not publish GitHub Pages on the free tier,
   and an unserved policy file protects nothing.
3. Settings → Pages → Source: Deploy from a branch → `main` → `/ (root)`.

## Proving it works

Fetch `https://196969.github.io/robots.txt` and confirm a **200** with the
body beginning `User-agent: *`. A 404 means the repository name is wrong or
Pages has not been enabled.

Verification at any other address proves the file exists, not that it
functions. That distinction is on the fault register.

## Honest limit

robots.txt is a request, not a control. Well-behaved crawlers honour it;
nothing enforces it. It does not make a public repository private — anything
served here remains readable by anyone holding the address.
