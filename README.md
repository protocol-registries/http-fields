# HTTP Field Name Registration Requests

This repository's issues list manages requests to add and change entries in the [HTTP Field Name Registry](https://www.iana.org/assignments/http-fields/). Please note our [contribution terms](.github/CONTRIBUTING.md).

Your [Experts](https://tools.ietf.org/html/rfc8126#section-4.6) are currently [@mnot](https://github.com/royfielding) and [@royfielding](https://github.com/royfielding).

See [the specification](https://www.ietf.org/archive/id/draft-ietf-httpbis-semantics-19.html#name-field-extensibility) for more information about the registration process and requirements for registration.

## When to Register

Registration is intended to:

1. Avoid conflicting uses of a field name
2. Allow the documentation associated with a field to be discovered
3. Offer guidance regarding a field's definition during the process of registration

It's not necessary to register fields that are only used in controlled deployments -- in particular, applications that don't need to interoperate with other implementations. This includes internal and private uses of HTTP, and HTTP APIs whose clients are specific to that service. However, these fields can still be registered (typically, as _provisional_) if you wish.

Generally, a registration request should be made when your document is mature enough for wide review. If your reference is an Internet-Draft, that means when it's adopted by a stream (e.g., the IETF stream, the Independent stream), not beforehand. If your reference is in another standards body, a request can be made before the document is finalised.

If your reference is from an Open Source project, community or commerical group, a request can be made once your document becomes public, but anticipatory requests are discouraged, and may be refused or delayed.

## Creating a Registration Reqeust

A registration request consists of the following template:

* **Field name**: The requested field name. It must conform to the field-name syntax defined in [Section 5.1 of the HTTP specification](https://httpwg.org/http-core/draft-ietf-httpbis-semantics-latest.html#fields.names), and should be restricted to just letters, digits, and hyphen (`-`) characters, with the first character being a letter.
* **Status**: "permanent", "provisional", "deprecated", or "obsoleted"
* **Specification document(s)**: Reference to the document that specifies the field, preferably including a URI that can be used to retrieve a copy of the document. Optional but encouraged for provisional registrations. An indication of the relevant section(s) can also be included, but is not required.
* **Comments**: Additional information, such as about reserved entries (optional).

### Choosing Your Field Name

[The HTTP specification](https://httpwg.org/http-core/draft-ietf-httpbis-semantics-latest.html#considerations.for.new.field.names) advises authors of specifications defining new fields to choose a short but descriptive field name. Short names avoid needless data transmission; descriptive names avoid confusion and "squatting" on names that might have broader uses.

To that end, limited-use fields (such as a header confined to a single application or use case) are encouraged to use a name that includes that use (or an abbreviation) as a prefix; for example, if the Foo Application needs a description field, it might use `Foo-Desc`; `Description` is too generic, and `Foo-Description-Field` is needlessly long.

While the field-name syntax is defined to allow any token character, in practice some implementations place limits on the characters they accept in field-names. To be interoperable, new field names should constrain themselves to alphanumeric characters, `-`, and `.`, and should begin with a letter. For example, the underscore (`_`) character can be problematic when passed through non-HTTP gateway interfaces.

Field names ought not be prefixed with `X-`; see [BCP178](https://www.rfc-editor.org/rfc/rfc6648.html) for further information.

Other prefixes are sometimes used in HTTP field names; for example, `Accept-` is used in many content negotiation headers, and `Content-` is used as explained in [Section 6.4 of HTTP](https://httpwg.org/http-core/draft-ietf-httpbis-semantics-latest.html#content). These prefixes are only an aid to recognizing the purpose of a field, and do not trigger automatic processing.

### Choosing the Right Status

Fields defined by standards-defined specificaions will have a status of "permanent"; most other fields will have a status of "provisional." See [the HTTP specification](https://httpwg.org/http-core/draft-ietf-httpbis-semantics-latest.html#fields.registry) for details.

### Suitable Specifiction Documents

Specification documents are required for permanent registration, and encouraged for provisional registrations. They need to be publicly available and reasonably stable. 

### Defining Field Semantics and Other Considerations

A checklist of important [considerations for new fields](https://httpwg.org/http-core/draft-ietf-httpbis-semantics-latest.html#considerations.for.new.fields) is available in the HTTP specification.

## Submitting Your Request

The request can be made by:

* [Filing an issue](https://github.com/protocol-registries/http-fields/issues/new/choose) (preferred), or
* Sending e-mail to [the mailing list](ietf-http-wg@w3.org).

Once approved, your request will be incorporated into the IANA registry, whereupon it will be officially registered.
