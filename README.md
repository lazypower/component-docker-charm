# Charm layer for docker

This charm is a very bare-bones layer that exposes Docker, a container runtime
to charm authors for use in a 'juju compose' format, where you can mix charms
together, to remix them into a new "final" charm state.

The component-docker layer will handle installing Docker from an upstream apt
repository, ensuring you're fetching the latest recommended Docker for your
distribution.

## Component Usage

TBD

## Notes

This particular component layer is just an adapted script from upstream Docker's
shell based installation script, located at https://get.docker.io

# Component Configuration

- `docker_user` - Assign a system user to the `docker` group. Allowing them to
    interface with the Docker daemon (without using sudo/su).

