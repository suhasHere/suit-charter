## Charter for Working Group
Vulnerabilities in Internet of Things (IoT) devices have raised the
need for a secure firmware update mechanism that is also suitable for
constrained devices. Security experts, researchers, and regulators
recommend that all IoT devices be equipped with such a mechanism. While
there are many proprietary firmware update mechanisms in use today, there
is a lack of a modern interoperable approach of securely updating the
software in IoT devices.

A firmware update solution consists of several components, including:
* A mechanism to transport firmware images to IoT devices.
* A manifest that provides meta-data about the firmware image
(such as a firmware package identifier, the hardware the package
needs to run, and dependencies on other firmware packages), as
well as cryptographic information for protecting the firmware
image in an end-to-end fashion.
* The firmware image itself.

RFC 4108 provides a manifest format that uses the Cryptographic Message
Syntax (CMS) to protect firmware packages.

More than ten years have passed since the publication of RFC 4108, and
greater experience with IoT deployments has led to additional
functionality, requiring the work done with RFC 4108 to be revisited.
This group will focus on defining a firmware update solution for Class
1 devices, as defined in RFC 7228, that is -- IoT devices with ~10 KiB
RAM and ~100 KiB flash. The solution may apply to more capable devices
as well. This group will not define any transport mechanisms.

In June of 2016 the Internet Architecture Board organized a workshop on
'Internet of Things (IoT) Software Update (IOTSU)', which took place at
Trinity College in Dublin, Ireland. The main goal of the workshop was
to foster a discussion on requirements, challenges, and solutions for
bringing software and firmware updates to IoT devices. This workshop 
also made clear that there are challenges with misaligned incentives
and complex value chains. It is nevertheless seen as important to 
create standard building blocks that help interested parties implement
and deploy a solid firmware update mechanism.

In particular this group aims to publish several documents, namely:
* An IoT firmware update architecture that includes a description of
the involved entities, security threats, and assumptions.
* One or more manifest format specifications.

The initial focus of this group will be development of a manifest approach based on CMS and the ASN.1 encoding. This work will result in a revision of RFC 4108 that reflects the current best practices. Use of the ASN.1 encoding is desirable due to existing ASN.1 support in crypto libraries used within current IoT operating systems. The group may later adopt alternate manifest formats using other serialization approaches (e.g., CBOR).
This group does not aim to create a standard for a generic software
update mechanism for use by rich operating systems, like Linux, but
instead this group will focus on software development practices in the
embedded industry. "Software update solutions that target updating
software other than the firmware binary (e.g. updating scripts) are
also out of scope.

This group will aim to maintain a close relationship with silicon vendors
and OEMs that develop IoT operating systems.
