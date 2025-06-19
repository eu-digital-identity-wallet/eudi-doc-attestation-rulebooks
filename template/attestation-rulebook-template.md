
# Attestation Rulebook template

## 1 Introduction

### 1.1 Document scope

Describe the scope of this document

### 1.2 Document structure

Describe the structure of this document

### 1.3 Key words

The following are the recommended keywords. Modify if necessary

This document uses the capitalised key words 'SHALL', 'SHOULD' and 'MAY' as
specified in [RFC 2119], i.e., to indicate requirements, recommendations and
options specified in this document.

In addition, 'must' (non-capitalised) is used to indicate an external
constraint, i.e., a requirement that is not mandated by this document, but, for
instance, by an external document. The word 'can' indicates a capability,
whereas other words, such as 'will', and 'is' or 'are' are intended as
statements of fact.

### 1.4 Terminology

It is recommended to use the terminology defined in Annex 1 of ARF. For example
the following text can be used. 

This document uses the terminology specified in Annex 1 of the ARF.

## 2 Attestation attributes and metadata

This section is used for defining all attributes than an
attestation of the defined type may contain. In this section
the attributes SHALL be defined in an encoding-independent manner (see ARB_06). 
Each attribute can be mandatory, optional, or conditional
and it SHALL be specified in the corresponding section (see ARB_09).

When attributes are defined, referring to attributes that
already exist in a catalogue of attestation attributes 
SHOULD be considered (see ARB_07).

Topic 9 of Annex 2 of the ARF defines the following High-Level Requirements with
respect to the Attestation Rulebooks

**Requirements for QEAA**
* An attribute as meant in Annex V point a)  of the [European Digital Identity Regulation] 
SHALL be included (see ARB_11). See also section 2.1. 
* One or more attributes or metadata representing the set of data meant in Annex 
V point b) of the [European Digital Identity Regulation] SHALL be included (see ARB_13)
* One or more attributes representing the set of data meant in Annex V point c)  
of the [European Digital Identity Regulation] SHALL be included (see ARB_16).
* One or more attributes or metadata representing the set of data meant in Annex V point e) 
of the [European Digital Identity Regulation] SHALL be included (see ARB_18).
* One or more attributes or metadata representing the location meant in Annex V point h)
of the [European Digital Identity Regulation] SHALL be included. This location SHALL 
indicate at least the URL at which a machine-readable version of the trust anchor to be
used for verifying the QEAA can be found or looked up (see ARB_20)

**Requirements for PuB-EAA**
* Αn attribute as meant in  Annex VII point a) of the [European Digital Identity Regulation] 
SHALL be included (see ARB_11). See also section 2.1.
* Οne or more attributes or metadata representing the set of data meant in Annex
 VII point b) of the [European Digital Identity Regulation] SHALL be included (see ARB_14).
* Οne or more attributes representing the set of data meant in Annex VII point c) 
of the [European Digital Identity Regulation] SHALL be included (see ARB_16).
* Οne or more attributes or metadata representing the set of data meant in Annex VII point e)
of the [European Digital Identity Regulation] SHALL be included (see ARB_18).
* one or more attributes or metadata representing the location meant in Annex VII point h)
of the [European Digital Identity Regulation] SHALL be included. This location SHALL 
indicate at least the URL at which a machine-readable version of the qualified 
certificate that signed the PuB-EAA can be found or looked up. (see ARB_20) 

**Requirements for non-qualified EAA**
* An attribute indicating that the attestation is an EAA should be included (see ARB_12).
See also section 2.1.
* Οne or more attributes or metadata representing the set of data meant in Annex 
V point b) of the [European Digital Identity Regulation] SHALL be included (see ARB_15).
* Οne or more attributes representing the set of data meant in Annex V point c) of the 
[European Digital Identity Regulation] SHOULD be included (see ARB_17))
* Οne or more attributes representing the set of data meant in Annex V point e) of 
the [European Digital Identity Regulation] SHOULD be defined (see ARB_19).
 * Οne or more attributes or metadata representing the location at which a machine-readable 
version of the trust anchor to be used for verifying the EAA can be found or
looked up SHOULD be defined. What this location indicates precisely is dependent 
on the nature of the mechanism used for distributing trust anchors, detailed in section 
2.6 (see ARB_21)

### 2.1 Introduction

Briefly introduce the design choice made for this attestation type. 

According to Annex V point a) and  Annex VII point a) of the [European Digital Identity Regulation]
an indication, at least in a form suitable for automated processing, that the attestation 
has been issued as a QEAA or Pub-EAA SHALL be defined. Similarly, according to ARB_12
of Annex 2 of the ARF a similar indication SHOULD be defined for non-qualified EAA.
This document defines the attribute "attestation_legal_category" which SHALL have
the value "QEAA" or "PuB-EAA" or "non-qualified-EAA". Sections 3,4,5 define the
corresponding formats. 

### 2.2 Mandatory attributes

| **Data Identifier** | **Definition** |
|------------------------|--------------|
| m_attribute_1 | First mandatory attribute|
| m_attribute_2 | Second mandatory attribute|


### 2.3 Optional attributes

| **Data Identifier** | **Definition** |
|------------------------|--------------|
| o_attribute_1 | First optional attribute|
| o_attribute_2 | Second optional attribute|

### 2.4 Conditional attributes

| **Data Identifier** | **Definition** |
|------------------------|--------------|
| c_attribute_1 | First conditional attribute|
| c_attribute_2 | Second conditional attribute|

### 2.5 Mandatory metadata 

| **Data Identifier** | **Definition** |
|------------------------|--------------|
| m_metadata_1 | First mandatory metadata (e.g., expiry date)|


### 2.6 Optional metadata 

| **Data Identifier** | **Definition** |
|------------------------|--------------|
| o_metadata_1 | First optional metadata (e.g., document number)|

### 2.7 Conditional metadata 

| **Data Identifier** | **Definition** |
|------------------------|--------------|
| c_metadata_1 | First conditional metadata |

### 2.8 Trust anchors

Mechanisms for the provision of a trust anchor that SHALL
be used for the verification of an attestation SHALL be defined in this section.
Furthermore,  for non-qualified EAA  in this section SHOULD  be defined (see ARB_26, ISSU_34):
* mechanisms allowing a Wallet Unit to verify that the EAA Provider is authorised 
or registered to issue this type of EAA.
* mechanisms allowing a Relying Party to obtain, in a trustworthy manner, the 
trust anchor(s) of the EAA Providers issuing this type of EAA.


### 2.9 Revocation
(see topic 7)
In this section information about the revocation mechanism used SHALL be defined. 

For PID, QEAA, or PuB-EAA it SHALL  be defined whether  only short-lived attestations 
will be used, having a validity period of 24 hours or less, such that revocation 
will never be necessary, or that the attestations are revocable. 

For revocable attestations it SHALL be defined which of the following methods must be implemented:
* Use an Attestation Status List mechanism included in a Technical Specification 
that will be specified by the Commission.
* Use an Attestation Revocation List mechanism included in a Technical Specification 
that will be specified by the Commission.
 

## 3 ISO/IEC 18013-5-compliant encoding 
If the attestation type supports the the format specified in ISO/IEC 18013-5,
then in this section the  ISO/IEC 18013-5-compliant encoding of attributes and metadata 
should be defined. 

It is noted that (see ARB_02) the Schema Provider SHALL analyse whether it must 
be possible for a User to present that type of attestation when the Wallet Unit 
and the Relying Party are in proximity and attestations are presented without 
using the internet. If so,the attestations must be issued in the ISO/IEC 18013-5-compliant 
mdoc format.

This section should include a table the data identifier specified in
Chapter 2,  the corresponding attribute identifier to be used in
presentation requests and responses according to [ISO/IEC 18013-5] and the encoding 
of each attribute. For example, 

| **Data Identifier** | **Attribute identifier** | **Encoding format** |
|------------------------|--------------|------------------|
| family_name | family_name | tstr |

The corresponding entry for the "attestation_legal_category" attribute defined
in Section 2.1 SHALL be:

| **Data Identifier** | **Attribute identifier** | **Encoding format** |
|------------------------|--------------|------------------|
| attestation_legal_category | attestation_legal_category | tstr |

A note proving more fine-grained requirements with respect to
the types SHOULD be defined (e.g., encoding, maximum lengths, 
date formats, etc). 

Additionally, in this section a document type SHALL be defined, which SHALL be 
unique within the scope of the EUDI Wallet ecosystem (see ARB_05).

Furthermore, when specifying new attributes existing conventions 
for attribute identifier values and attribute syntaxes SHOULD
be considered (see ARB_07).

Each attribute SHALL be defined within an attribute namespace. An attribute namespace 
SHALL fully define the identifier, the syntax, and the semantics of each attribute 
within that namespace. An attribute namespace SHALL have an identifier that is 
unique within the scope of the EUDI Wallet ecosystem, and each attribute 
identifier SHALL be unique within that namespace (see ARB_06a) A domestic namespace MAY defined 
to specify attributes that are specific to this Rulebook and are not included in 
the applicable EU-wide or sectoral namespace (see ARB_10). 

Finally, illustrative examples SHOULD be included. 

## 4 SD-JWT VC-based encoding 
If the attestation type supports the the format specified in "SD-JWT-based Verifiable 
Credentials (SD-JWT VC)", then in this section the  SD-JWT VC-compliant encoding 
of attributes and metadata should be defined. It SHALL be ensured that the attestations 
comply with the 'SD-JWT VCs' profile specified in [HAIP] (see ARB_01b).

It is noted that a  Schema Provider  MAY specify in the Attestation 
Rulebook that that type of attestation must be issued in the [SD-JWT VC]-compliant 
format, provided the [SD-JWT VC] specification has been approved by an EU standardisation 
body or by the European Digital Identity Cooperation Group established pursuant to 
Article 46e(1) of the [European Digital Identity Regulation] (see ARB_03).

In this section, a Verifiable Credential Type (`vct`) SHALL be defined,
which SHALL be unique within the scope of the EUDI Wallet ecosystem (see ARB_05).

Additionally,  when specifying new attributes existing conventions 
for attribute identifier values and attribute syntaxes SHOULD
be considered (see ARB_07).

It SHALL be ensured that each claim name is either included in the IANA registry 
for JWT claims, or is a Public Name as defined in [RFC 7519] (see ARB_06b). 

IANA registered claims should be presented in table that
includes their data identifier, attribute identifier, 
encoding format, and reference or note. For example,

| **Data Identifier** | **Attribute identifier** | **Encoding format** |**Reference/Notes** |
|-------------------- |--------------------------|---------------------|--------------------|
| family_name | family_name | string | Section 5.1 of [OIDC] |

A similar table should be used for Private Names specific
to the attestation type defined in this document. For
example:

| **Data Identifier** | **Attribute identifier** | **Encoding format** | **Notes** |
|---------------------|--------------------------|---------------------|-----------|
| expiry_date | date_of_expiry | string | ISO 8601-1 [ISO8601‑1] YYYY-MM-DD format, as defined in Section 5.4.4.2 of [EKYC Schema] |

The corresponding entry for the "attestation_legal_category" attribute defined
in Section 2.1 SHALL be:

| **Data Identifier** | **Attribute identifier** | **Encoding format** | **Notes** |
|---------------------|--------------------------|---------------------|-----------|
| attestation_legal_category | attestation_legal_category | string | Defined in Attestation Rulebook template |


Finally, illustrative examples SHOULD be included. 

## 5 W3C Verifiable Credentials Data Model-based encoding
If the attestation type supports the the format specified in W3C Verifiable Credentials 
Data Model, then in this section the  corresponding encoding  of attributes and 
metadata should be defined. 

It is noted that only a a non-qualified EAA can use this format (see ARB_01a)

Tables similar to the ones specified in section 4 SHALL be defined.

This section SHALL reference one or more documents specifying in detail how a 
Relying Party can request attributes from a such an attestation, and how a User 
can selectively disclose attributes from such an attestation. Moreover, these 
referenced documents SHALL be approved by an EU standardisation body or by the European 
Digital Identity Cooperation Group established pursuant to Article 46e(1) of the 
[European Digital Identity Regulation] (see ARB_04).

## 6 Attestation usage
Here it SHOULD  be specified whether a Relying Party receiving the attestation
must request and verify a PID (see ARB_27).

Furthermore, in this section information about potential transactional data
SHALL be defined (see Topic 20).

## 7 References
| **Item Reference** | **Standard name/details**|
|--------------------|---------------------------|
| [European Digital Identity Regulation] | [Regulation (EU) 2024/1183](https://eur-lex.europa.eu/legal-content/EN/TXT/HTML/?uri=OJ:L_202401183) of the European Parliament and of the Council of 11 April 2024 amending Regulation (EU) No 910/2014 as regards establishing the European Digital Identity Framework |
| [ISO/IEC 18013-5] | [ISO/IEC 18013-5](https://github.com/eu-digital-identity-wallet/eudi-doc-standards-and-technical-specifications/issues/84), Personal identification --- ISO-compliant driving licence - Part 5: Mobile driving licence (mDL) application |
| [SD-JWT VC] | [SD-JWT-based Verifiable Credentials](https://github.com/eu-digital-identity-wallet/eudi-doc-standards-and-technical-specifications/issues/9) (SD-JWT VC). Retrievable from: <https://datatracker.ietf.org/doc/draft-ietf-oauth-sd-jwt-vc/> |
| [W3C VCDM v2.0] | Sporny, M. *et al,* [Verifiable Credentials Data Model v2.0](https://github.com/eu-digital-identity-wallet/eudi-doc-standards-and-technical-specifications/issues/115), W3C Recommendation |
| [HAIP] | Yasuda, K. et al, "[OpenID4VC High Assurance Interoperability Profile](https://github.com/eu-digital-identity-wallet/eudi-doc-standards-and-technical-specifications/issues/4)", OpenId Foundation. |
| [IANA-JWT-Claims] | IANA JSON Web Token Claims Registry. Available: <https://www.iana.org/assignments/jwt/jwt.xhtml> |







 

