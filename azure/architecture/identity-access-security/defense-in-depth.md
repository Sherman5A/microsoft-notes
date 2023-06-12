
# Defense-In-Depth

[[defense-depth.png]]

Defense-in-depth,

> Series of mechanism that aims to slow the advance of an attack that aims to get unauthorised access
  to data.

Each layer is put in place to prevent further exposure. There is no reliance on only a single layer of
protection.

It slows down an attacker, so that the security team can prepare and act against the attacker.

## DiD Layers

Role of each layer,
- Physcial Security - **Defends the hardware in the data center**
    - Securing access to building
    - Ensure that other layers can't be bypassed
- Identity & Access - **Controls access to infrastructure and change control**
    - Access is only granted when needed
    - Identities are secure and authenticated
    - Sign-ins are logged and audited
- Perimeter - **DDoS protection filters large-scale attacks before they can reduce availability for
                users**
    - Protects from network-based attacks
    - Perimiter firewalls identify and altert when malicious attacks happen
- Network - **Limits communication between resources through segmentation and access control**
    - Resources only have access to whats required
    - Limiting communication reduces the risk of an attack spreading to other resources
    - Restrict inbound and outbound access
    - Deny by default
- Compute - **Secures access to VMs**
    - Keep systems patched and current
    - Secure VM access
    - Computer resources are secure
- Application - **Ensures applications are free of security vulnerabilities**
    - Ensure applications are secure
    - Sensitive data is stored securely
- Data - **Controls access to business and customer data**
    - Controls and processes must be put into place to ensure integrity, confidentiality

