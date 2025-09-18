# Security FAQ

Still not finding what your looking for? Contact us at [support@littlearms.com](mailto:support@littlearms.com) with your support question.  We will respond as soon as we receive your message.

<details>

<summary>What is Little Arms Studios?</summary>

Little Arms Studios is a tech startup incorporated in the USA 🇺🇸

&#x20;as `Little Arms Studios Inc.`

</details>

<details>

<summary>Where and how is my data stored?</summary>

All user data and content is stored in the USA 🇺🇸 on [Amazon Web Services (AWS)](https://aws.amazon.com), which is backed by the same infrastructure and security that Amazon uses for its own services.

Customer data is stored in USA data centers.  The website [https://zephyr-sim.com](https://zephyr-sim.com) and its assets may be cached in other geographic locations by AWS's CDN service CloudFront.

Access to private content through [https://zephyr-sim.com](https://zephyr-sim.com) is always validated through our API using a permission system.

Amazon's AWS follows and leads most of the industries best practices and is [compliant with major security standards](https://aws.amazon.com/compliance/resources/).

</details>

<details>

<summary>Is customer data encrypted?</summary>

Yes all customer data is encrypted at rest and in-transit.

* In transit we use HTTPS TLS 1.2 to encrypt all traffic served to end users.
* At rest on Amazon Web Services (AWS) we use AES-256

</details>

<details>

<summary>What web/IP addresses/ports need to be whitelisted to access the site and sim?</summary>

* littlearms.com
* \*.littlearms.com
* zephyr-sim.com
* \*.zephyr-sim.com
* https://littlearms.us.auth0.com
* port 443

</details>

<details>

<summary>How are users authenticated?</summary>

By default, all customer data can only be accessed by themselves or Little Arms Studios Administrators.  If a customer accepts an invitation to join an Organization as a Student, then their data can be access by the Instructors or Administrators of that Organization.

Customers may also choose to make some of their data public on their personal profile to showcase their flight time, achievements and obtained certifications.

</details>

<details>

<summary>Which data is required to operate on Zephyr?</summary>

The only required piece of information to sign up and start using Zephyr is an **email address.**

When purchasing a Certification test such as the BPERP, personal information such as first name, last name and email address is required and provided to the [Airborne Public Safety Association](https://publicsafetyaviation.org/apsa-basic-proficiency-evaluation-for-remote-pilots-bperp-certificate-application), which review and approve the BPERP certification.

</details>

<details>

<summary>Proxy issues</summary>

Errors due to proxy misconfiguration can manifest myriad ways, but the most common issue would be "Zephyr received a set of invalid credentials" when trying to launch Zephyr from the Little Arms Launcher.

Typically this is due to the way the simulator interprets the `HTTPS_PROXY` environment variable on some computers. If you have a program that manages your proxy settings, it can create multiple values for this `HTTPS_PROXY` environment variable.

At this time, the simulator can only interpret one URL value in this environment variable. For example `HTTPS_PROXY=xyz-xyz.domain.com:80`. If this value has multiple URL's (for example `HTTPS_PROXY=xyz-xyz.domain.com:80;abc-abc.domain.com:80`, the simulator will error when trying to communicate to our API.

Until we can fix this issue in the simulator, you will need to resolve this issue by either:

1. Remove the `HTTPS_PROXY` value from your environment variable
2. Ensure the `HTTPS_PROXY` value is a single URL

</details>
