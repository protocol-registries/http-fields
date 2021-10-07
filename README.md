# HTTP Field Name Registration Requests

This repository's issues list manages requests to add and change entries in the [HTTP Field Name Registry](https://www.iana.org/assignments/http-fields/). Please note our [contribution terms](.github/CONTRIBUTING.md).

Your [Expert](https://tools.ietf.org/html/rfc8126#section-4.6) is currently [EXPERT_GITHUB_ID](EXPERT_GITHUB_LINK).

See [RFC_NUMBER](RFC_LINK) for more information; in particular, the [requirements for registration](RFC_REQUIREMENTS_LINK).


## When to Register

Registration is intended to:

1. Avoid conflicting uses of a field name
2. Allow the documentation associated with a field to be discovered
3. Offer guidance regarding a field's definition during the process of registration

It's not necessary to register fields that are only used in controlled deployments -- in particular, applications that don't need to interoperate with other implementations. This includes internal and private uses of HTTP, and HTTP APIs whose clients are controlled by the service. However, these fields can still be registered (typically, as _provisional_) if you wish.

Generally, a registration request should be made when your document is mature enough for wide review. If your reference is an Internet-Draft, that means when it's adopted by a stream (e.g., the IETF stream, the Independent stream), not beforehand. If your reference is in another standards body, a request can be made before the document is finalised.

If your reference is from an Open Source project, community or commerical group, a request can be made once your document becomes public, but anticipatory requests are discouraged, and may be refused or delayed.

## How to Register

A registration request consists of the following template:

* **Field name**: The requested field name. It must conform to the field-name syntax defined in [Section 5.1 of the HTTP specification](https://httpwg.org/http-core/draft-ietf-httpbis-semantics-latest.html#fields.names), and should be restricted to just letters, digits, and hyphen ('-') characters, with the first character being a letter.
* **Status**: "permanent", "provisional", "deprecated", or "obsoleted"
* **Specification document(s)**: Reference to the document that specifies the field, preferably including a URI that can be used to retrieve a copy of the document. Optional but encouraged for provisional registrations. An indication of the relevant section(s) can also be included, but is not required.
* **Comments**: Additional information, such as about reserved entries (optional).

Fields defined by standards-defined specificaions will have a status of 'permanent'; most other fields will have a status of 'provisional.' See [the HTTP specification](https://httpwg.org/http-core/draft-ietf-httpbis-semantics-latest.html#fields.registry) for details.

The request can be made by:

* [Filing an issue](https://github.com/protocol-registries/http-fields/issues/new/choose) (preferred), or
* Sending e-mail to [the mailing list](ietf-http-wg@w3.org).

Once approved, your request will be incorporated into the IANA registry, whereupon it will be officially registered.
