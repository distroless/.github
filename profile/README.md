
![distroless logo](https://github.com/distroless/.github/raw/main/profile/distroless-logo.svg)

A distroless image contains only an application and its runtime dependencies; that is, it is a minimal image without a shell or package manager.

We use [apko](https://github.com/chainguard-dev/apko) and [melange](https://github.com/chainguard-dev/melange) as our distroless build system. Combined, these tools provide for a reproducible, declarative approach to building OCI images. 

**melange** lets you build APKs using declarative YAML pipelines. _APKs_ are `.apk` packages compatible with the package manager used by Alpine, similar to `.deb` or `.rpm` for instance.

**apko** lets you bundle a collection of APKs into an OCI image using a declarative YAML manifest.

Our distroless images provide SBOM support and signatures for known provenance and more secure base images. They can be part of an approach to a secure software factory.

## Find and use distroless images

Our distroless images are available via [distroless.dev](https://distroless.dev).

You can pull down a distroless image with Docker, for example:

```sh
docker pull distroless.dev/apko
```

Because all distroless images are signed with [Cosign](https://docs.sigstore.dev/cosign/overview), you can check the signature. For our apko image example, you can run the following:

```sh
COSIGN_EXPERIMENTAL=1 cosign verify distroless.dev/apko | jq
```

Your output will indicate that the Cosign claims were validated. 

## Contribute a distroless image

If you are interested in contributing a new distroless image, you can base it off of our [template](https://github.com/distroless/template). Please refer to the [Readme](https://github.com/distroless/template#template-repository-for-distroless-images) for further guidance.

## Learn more

You can learn more about distroless images, apko, and melange from the following articles:

* [Introducing apko: bringing distroless nirvana to Alpine Linux](https://blog.chainguard.dev/introducing-apko-bringing-distroless-nirvana-to-alpine-linux/)
* [Minimal Container Images: Towards a More Secure Future](https://blog.chainguard.dev/minimal-container-images-towards-a-more-secure-future/)
* [Secure Your Software Factory with melange and apko](https://blog.chainguard.dev/secure-your-software-factory-with-melange-and-apko/)

## Media

Find the distroless logo, artwork, and brand guidelines in the [distroless/artwork](https://github.com/distroless/artwork) repository. 
