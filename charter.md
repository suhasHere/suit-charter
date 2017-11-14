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

## WG Objectives
This WG will work on developing a interoperable secure firmware upgrade solution for IoT devices that are constrained in resources (such as RAM, Flash). The solution must enable such an upgrade for the IoT devices under various deployment options (such as, deployments under constrained network access typically controlled by an Enterprise IT deparment as well as open Internet access deployments). 

An extensible manifest format to describe metadata about the firmware and its security properties will be developed by this WG. The solution must enable the IoT devices to locate the manifest and the update server via existing transport protocol mechanisms.

In paritcular, this WG will perform  the following work:
1. Document that defines the requirements for secure firmware upgrade solution.
2. Define a general architecture that enables secure IoT firmware 
upgrade describing involved elements, security threats, update server discovery and assumptions.
3. Document that describes data model for elements that captures 
metadata and security properties about the firmware in the form of a manifest.
4. Define one or more encoding formats for the manifest.
5. Document describing use of exising transport and protocol mechanisms to locate and download the firmware.
6. A best current practices document that defines firmware installation process on the IOT device.

This group does not aim to create a standard for a generic software
update mechanism for use by rich operating systems, like Linux, but
instead this group will focus on software development practices in the
embedded industry. "Software update solutions that target updating
software other than the firmware binary (e.g. updating scripts) are
also out of scope.

This group will aim to maintain a close relationship with silicon vendors
and OEMs that develop IoT operating systems.
