# When Custom Job Is Required: Common Scenarios

Most migration projects work well with standard capabilities when the source and target platforms can represent the same store meaning in similar ways. A **Custom Job** becomes necessary when “standard migration” can move the records, but cannot preserve a specific business-critical structure, relationship, or data type your store relies on.

This article explains what a Custom Job is in practical terms, the most common scenarios that trigger custom requirements, and how to confirm the need early using the refined migration journey.

### What is Custom Job

A **Custom Job** is a modification or extension of the migration tool designed to handle a special requirement that standard capabilities cannot cover. It is targeted custom handling used when one of these is true:

* The data exists, but the target platform cannot represent it the same way by default
* The data is stored in a third-party system, plugin, or custom fields rather than native entities
* The data must be transformed to preserve meaning, behavior, or customer experience

The purpose of a Custom Job is not “extra help.” It is to make the migration technically capable of preserving what matters when standard migration cannot.

If you are still deciding which service level fits your project, **\[How to Choose Next-Cart Migration Service Model]** provides a clean decision framework based on complexity, internal capacity, and risk ownership.

### Common scenarios that require a Custom Job

### Scenario 1: Your store relies on third-party apps or extensions that add important data

This is the most common trigger.

Signs you might need a Custom Job:

* product data includes non-standard specification blocks or custom attributes used for filtering
* orders contain custom metadata used for operations, fulfillment, or reporting
* customer records include tags, groups, or custom fields that drive segmentation
* media fields are stored outside standard product image structures

How to confirm early:

* include products and orders that rely on these extensions in your demo sample
* review whether the resulting target data preserves business meaning, not just whether “something transferred”

### Scenario 2: You need to migrate custom fields that are not natively supported on one side

Even if your source platform supports a field, the target platform may not represent it the same way by default.

Common examples:

* special price types that exist in the source but not natively in the target
* extra product attributes added through an extension
* custom order fields needed for back-office workflows
* custom customer fields used for B2B or segmentation logic

Why it matters:

If the target platform cannot represent these fields without customization, the data may be omitted, flattened into generic text, or mapped in a way that loses usefulness. That is usually where a Custom Job becomes necessary.

### Scenario 3: You need data filtering rather than a full-scope migration

Filtering is a strategic choice. Many stores do not want to migrate everything.

Filtering requests that commonly require a Custom Job:

* migrate only active products
* migrate only in-stock products
* migrate only products from specific categories
* migrate only orders after a specific date
* migrate only customers who have placed at least one order
* migrate only blog posts published after a certain date

When filtering is most useful:

* you are reducing scope intentionally for a phased launch
* you are cleaning up legacy catalog clutter
* you want to avoid migrating historical records that have no operational value

Planning note:

Filtering should be defined before full execution. The earlier you decide, the less rework you create during validation.

### Scenario 4: You need transformation, cleanup, or restructuring during migration

Sometimes you want the migration to improve the target store’s structure, not just copy the old store.

Examples of transformation-oriented Custom Jobs:

* remove unwanted patterns from product descriptions or standardize formatting
* convert certain attribute sets into a structure that the target platform supports better
* reshape category or grouping logic so the target browsing experience matches intent
* normalize option values so variants behave predictably (size and color consistency)

When this is a good idea:

* when the old store contains workarounds that will not translate cleanly
* when “copy as-is” would create a confusing storefront on the target platform

### Scenario 5: You have a Custom Cart requirement

A “Custom Cart” situation can include:

* a platform not currently on the supported list
* a heavily customized self-hosted implementation
* unique data storage patterns that require special handling

These situations often require a Custom Job because the migration needs to interpret or map data structures that are not standard for a typical platform pairing.

### Scenario 6: Your migration needs require special handling to preserve relationships

Relationship issues can appear when:

* products and variants are structured in a non-standard way
* categories or collections are used as operational tags rather than browse pathways
* extensions store relationships outside the default platform model

If relationships are not preserved, the store can look migrated but behave incorrectly, especially in discovery and conversion paths.

### How to tell from demo results if you need a Custom Job

Use these signals to avoid guessing:

#### Strong signals (likely custom requirement)

* business-critical fields are missing or unusable on the target platform
* app-driven behavior disappears in a way that affects conversion or operations
* product options/attributes lose meaning and cannot be represented through standard mapping
* you are migrating to/from a platform outside the supported list

#### Moderate signals (could be mapping or platform differences)

* data is present but displayed differently
* category organization looks different but may be fixable through mapping decisions
* some fields appear in a different place or format

The safest approach is to classify each concern as one of four types:

* mapping decision
* scope decision
* platform capability difference
* custom requirement (Custom Job)

**Expert insight**: Many teams assume they “need customization” when they really need clarity. But when a requirement is truly custom, treating it as “we’ll fix it later” creates the highest risk. Custom needs should be identified early so the migration plan is built on what is actually possible.

#### How Custom Jobs relate to demo vs paid experience

Custom data migration is not part of the demo experience. That is intentional: the demo is meant to evaluate direction using limited sample data and reveal whether custom handling is required.

Once custom needs are confirmed, Custom Jobs are planned as part of the paid Custom Migration experience so outcomes can be validated reliably.

**Important note**: which entity types are available for migration can vary depending on the source and target platform capabilities. Custom handling decisions should be based on your platform pairing and your store’s requirements, not on a generic list of entities.

### Conclusion

Custom Jobs are required when default migration capabilities cannot preserve the outcomes your business needs, especially when important data lives in extensions, custom fields, or non-standard structures. The safest way to identify the need is to run a representative Demo Migration and review results with an outcome lens: does the target store still behave correctly in buying paths, discovery, promotions, and operations. When a Custom Job is truly needed, it is best treated as a planned requirement early, not a late fix under go-live pressure.

If you suspect your store relies on extensions, custom fields, or filtering rules, build a demo sample that includes those exact items and run a Demo Migration to reveal what standard capabilities can and cannot preserve. If you want expert help identifying whether a Custom Job is required and what scope should be customized to protect your launch outcomes, reach out via Live Chat. Next-Cart can help you confirm requirements early and choose the safest service model before timelines tighten.

#### FAQs

<details>

<summary><strong>Does needing Custom Jobs mean my data cannot be migrated otherwise?</strong></summary>

Not necessarily. Many stores can migrate core data, but custom scope is about whether the result will behave correctly and match the outcomes you require. Custom handling is used when standard mapping cannot reliably reach that outcome.

</details>

<details>

<summary><strong>What is the most common cause of “surprise” custom scope?</strong></summary>

App-driven or custom-field data discovered late. Teams often assume a feature is native because it looks native in the storefront, then learn it is powered by a third-party system that requires special planning.

</details>

<details>

<summary><strong>How can I tell early if I will need Custom Jobs?</strong></summary>

Use a Demo Migration with a deliberately complex sample: best sellers, variant-heavy products, high-traffic categories, and representative orders.

Validate behavior, not only totals. If the outcome depends on data outside standard entities or requires transformation logic, custom handling becomes likely.

</details>

<details>

<summary><strong>Can Custom Jobs fix messy source data automatically?</strong></summary>

Some issues can be handled through mapping decisions or custom handling, but the best outcomes usually come from fixing inconsistent patterns at the source when possible.

Custom Jobs are most valuable when they preserve business-critical meaning, not when they replace basic cleanup.

</details>

<details>

<summary><strong>Should I decide on Custom Migration before testing a demo?</strong></summary>

Usually no. If you are uncertain, a demo-first approach is safer. Demo results often reveal whether your project behaves like a standard case, needs higher-touch guidance, or requires custom handling to reach the outcomes you care about.

</details>

<details>

<summary><strong>If my demo results show missing data, does that always mean I need a Custom Job?</strong></summary>

Not always. Missing or unexpected outcomes can be caused by mapping decisions, scope assumptions, or platform capability differences. The best next step is to classify the issue and review a representative sample with an expert to confirm whether customization is truly required.

</details>
