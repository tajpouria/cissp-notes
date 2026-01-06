# CISSP Exam Prep Notes

### CIA Triad

- **C (Confidentiality)**: Access control to ensure that only authorized subjects can access objects.
- **I (Integrity)**: Ensure that data or systems are not modified without authorization.
- **A (Availability)**: Authorized requests for objects must be granted to subjects in a reasonable time frame.

### ISC2 Code of Ethics

1. Protect society, the common wealth, and the infrastructure.
2. Act honorably, honestly, justly, responsibly, and legally.
3. Provide diligent and competent service to principals.
4. Advance and protect the profession.

<!-- TODO: Read the entire ISC2 Code of Ethics and summarize key points -->

## Domain 1: Risk Management & Risk Analysis

### Security Policy Development

There are four levels of security policy development:

1. **Level 1**: Acceptable Use Policy
   Design to assign roles within the organization and tie responsibilities to those roles.
2. **Level 2**: Security Baselines
   Defines "Minimum level" of security that every system in the organization must meet.
3. **Level 3**: Security Guidelines
   Offer recommendations on how standards and baselines must be implemented.
4. **Level 4**: Security Procedures
   The step-by-step instructions for implement a solution for protection our data or infrastructure.

> When you are developing a new safe guard, that means that you establishing a new security baseline, which means maintaining compliance with the existing baseline is not a valid consideration.

#### Risk Categories (Group of potential causes of risk)

- **Damage**: Physical damage to assets or the inability to access them.
- **Disclosure**: Disclosing of the sensitive information regarding of where and how it was disclosed.
- **Loss**: These might be temporary or permanent loss of assets. It could include altered data or inaccessible data.

#### Risk Factors (Something that increases the risk or susceptibility)

- **Physical Damage**: Natural cause, power loss, vandalism, theft.
- **Malfunction**: Failure of the systems, networks or peripherals.
- **Attacks**: Purposeful acts wether from inside or outside such as unauthorized disclosure.
- **Human Error**: Usually considered unintentional, such as misconfiguration or improper use.
- **Application Error**: Failure of the application, including the operating system.

#### Security Planning

Must include 3 types of the plans:

1. **Strategic**: Long term, stable plan that should include risk assessment. (5 years horizon, updated annually)
2. **Tactical**: Mid-term plan developed to provide more details on the goals of the strategic plan. (1 year horizon, updated semi-annually)
3. **Operations**: Short-term plan that is highly detailed based on the tactical and strategic plans. (monthly, quarterly updates)

#### Response to Risk

- **Risk Acceptance**: Accept the risk and potential loss if treat occurs.
- **Risk Mitigation**: Implement countermeasures and accepting the residual risk. (Not every risk can be mitigated)
- **Risk Assignment**: Transfer the risk to a third party (e.g., insurance).
- **Risk Avoidance**: When cost of mitigation or accepting is higher than the benefits of the service.
- **Risk Deterrence**: Implement controls to discourage or make attacks less attractive to potential threat actors. (e.g., warning signs, security guards, auditing)
- **Risk Rejection**: An **Unacceptable** possible response to risk to reject or ignore the risk.

> Handling the risk is not one-time process.

### Risk Management Frameworks (RMF)

#### NIST 800-37 (The primary risk management framework reference in CISSP)

Here's 7 steps of NIST RMF:

1. **Prepare** to execute the RMF
2. **Categorize** the information systems
3. **Select** security controls
4. **Implement** security controls
5. **Assess** security controls
6. **Authorize** the system
7. **Monitor** security controls

> When multiple priorities are present, **Human Safety** is always the most important.
> When legal issues are involved, "calling an attorney" is a valid choice.

#### Types of Risks

- **Residual Risk**: The risk that remains event after all of the conceivable safeguards are in place. The risk management has chosen to accept rather than mitigate. _AFTER_
- **Inherent Risk**: Newly identified risk that is not yet addressed with risk management strategies. The amount of the risk that exists in the absence of controls. _BEFORE_
- **Total Risk**: The amount of risk an organization would face if **no safeguards** were implemented. _WITHOUT_

<!-- TODO: Be able to explain total risk, residual risk, and controls gap -->

To calculate **TOTAL RISK**, know this formula

`total risk = threats * vulnerabilities * asset value`

**RISK** can be defined as follows:

`risk = threat * vulnerability`

#### Risk Analysis

There are two primary ways to evaluate risk to assets:

##### **Quantitative Risk Analysis**

Assigns a **dollar value** to evaluate effectiveness of countermeasures. _OBJECTIVE_ because it is based on measurable data.

Steps:

1. **Inventory assets** and assign a asset value (**AV**)
2. **Identify threats**. Research each asset and produce a list of all possible threats of each asset. Then calculate the **Exposure Factor (EF)** and **Single Loss Expectancy (SLE)** for each threat.
3. **Perform a threat analysis** to calculate the likelihood of each threat being realized within a single year. This is called the **Annual Rate of Occurrence (ARO)**.
4. **Estimate the the potential loss** by calculating the annualized loss expectancy (**ALE**).
5. **Research countermeasures for each threat**, and then calculate the changes to **ARO** and **ALE** based on an applied countermeasure.
6. **Perform cost-benefit analysis** of each countermeasures for each threat for each asset.

##### **Qualitative Risk Analysis**

Uses a **scoring system** to rank threats, and effectiveness of countermeasures. _SUBJECTIVE_ because it involves opinions.

> **DELPHI Technique** is an anonymous feedback-and-response method often used in qualitative risk analysis to gather opinions from experts without allowing any one individual to dominate the discussion.

#### Risk analysis consolations

- **Loss potential**: What would be the loss if the threat agent is successful in exploiting a vulnerability.
- **Delayed loss**: The amount of loss that can occur over time.

> **Treat Agents** are what cause treats by exploiting vulnerabilities.

#### Important Elements in Quantifying Potential Loss

- **Exposure Factor (EF)**: **Percentage** of loss that an organization would experience if a specific assess violated by a realized risk.
- **Single Loss Expectancy (SLE)**: The **monetary value** associated with a single realized risk against a specific asset. `SLE = Asset Value (AV) * Exposure Factor (EF)` (.e.g $10,000 \* 25% = $2,500)
- **Annual Rate of Occurrence (ARO)**: The **expected frequency** with which a specific threat or risk will occur within a single year.
- **Annualized Loss Expectancy (ALE)**: The yearly **monetary value** of all instances a specific realized threat against a specific asset. `ALE = Single Loss Expectancy (SLE) * Annual Rate of Occurrence (ARO)`

  > For example let's we have a office building with an asset value of $10,000,000. If a fire were to occur, it would cause an exposure factor of 25%. And fire is expected to occur once every 10 years (10%):

  ```
  SLE = $10,000,000 * 25% = $2,500,000
  ALE = $2,500,000 * 10% = $250,000
  ```

- **Safeguard Evaluation**: Good security controls **mitigate risk**, are **transparent** to users, **difficult to bypass** and are **cost effective**.

`value of the safeguard = ALE before safeguard - ALE after safeguard - annual cost of safeguard`

- **Controls Gap**: he amount of risk reduced by implementing safeguards.

`residual risk = total risk - controls gap`

#### Applying Risk-Based Management Concepts to **Supply Chain**

Today, most services are delivered thorough a chain of multiple entities. Each entity in the supply chain can introduce risk to the overall service delivery.
A secure supply chain includes vendors who are secure, reliable, trustworthy, and reputable.

##### Supply chain evaluation
