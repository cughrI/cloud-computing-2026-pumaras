# Two-Tier Architecture

A two-tier architecture splits an application into two layers that run separately
but work together: a web/application tier and a database tier.

## The Web/Application Tier
This tier is what users interact with. It serves the user interface, handles HTTP
requests, and runs the application logic. In this lab, the Nextcloud container is
the web/application tier, reachable in the browser on port 8080.

## The Database Tier
This tier stores persistent data such as user accounts, credentials, and file
metadata. The data must survive page reloads and restarts. In this lab, the
MariaDB container is the database tier.

## Why separate them?
Separating the tiers lets each one be updated, restarted, scaled, and secured
independently, so a problem in one container does not take down the other. It also
follows the one-service-per-container practice, which makes each part easier to
maintain, back up, and replace than a single container holding everything.
