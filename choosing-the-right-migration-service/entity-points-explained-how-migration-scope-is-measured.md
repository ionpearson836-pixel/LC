# Entity Points Explained: How Migration Scope Is Measured

Migration pricing often feels confusing because raw counts can be misleading. Two stores might have the same number of products, but the effort and risk can be very different once you factor in order history, customer records, and how much “connected data” needs to stay consistent after the move.

Next-Cart uses **Entity Points** to make migration scope easier to estimate and easier to compare across stores.

### What are Entity Points?

**Entity Points** are a weighted method of measuring migration scope based on four core data types that drive most migration workload:

* Products
* Orders
* Blog posts
* Customers

Instead of treating every record as equal, Entity Points apply different weights to reflect real-world complexity.

### How Entity Points are calculated

Each core entity type has a coefficient:

* Products: **1.0**
* Orders: **0.8**
* Blog posts: **0.6**
* Customers: **0.5**

{% code overflow="wrap" fullWidth="false" %}
```
Entity Points = (Products × 1.0) + (Orders × 0.8) + (Blog posts × 0.6) + (Customers × 0.5)
```
{% endcode %}

#### **Example calculation**

If your store has:

* 500 products
* 600 orders
* 100 blog posts
* 100 customers

Entity Points = (500 × 1.0) + (600 × 0.8) + (100 × 0.6) + (100 × 0.5)\
\= **1,090 Entity Points**

That total helps you choose an Entity Points plan sized for a single migration run.

### What Entity Points include and what they do not

A common misconception is that Entity Points represent everything that migrates. They do not.

Entity Points are a sizing method based on the “big four” drivers. Supporting data may still be migrated as part of scope (depending on platform support), but it does not increase the Entity Points calculation.

This distinction matters because many migration challenges come from “behavior continuity”, not just “data presence”.

For example, carrying over data tied to third-party systems or custom fields often requires more planning than standard catalog records.

If you are unsure whether your store falls into that category, **When Custom Job Is Required: Common Real-World Scenarios** is the best place to confirm what usually needs customization.

### Entity Points plans are licensed for a specific platform pairing

Your Migration Service and Entity Points Plan apply to a specific direction:

**Source → Target**

For example, a plan purchased for **Shopify → WooCommerce** applies only to that direction. It cannot be reused for **WooCommerce → Shopify** or for a different target platform.

This is one of the reasons Next-Cart recommends validating early. If you want to confirm how key entities map in your exact platform pairing, **Demo Migration: What It Proves and How to Read Results** is often the fastest starting point.

### Entity Points apply per migration run

Entity Points apply per individual migration run. They are not a lifetime pool that gets consumed.

This matters because many projects follow a pattern like:

* Full Migration first, then
* one or more **Recent Data Migrations** closer to go-live to sync newer orders, customers, or products

You can run Recent Data Migration multiple times as long as each run stays within your plan’s Entity Points. If you are planning a launch window and want to avoid gaps in recent orders or customer activity, **Recent Data Migration: Final Sync Before Go-live** explains how teams typically handle that final synchronization.

#### How pricing scales for extremely large migrations

For very large migration runs, additional upgrade logic can apply.

If a plan surpasses **1,024,000 Entity Points**, an additional **$50** is charged for each extra **100,000 Entity Points**.

### Best practices for accurate sizing

A reliable Entity Points estimate comes from real store totals, not rough guesses:

* Pull product, customer, order, and blog post counts from your current admin
* Treat Entity Points as a planning tool, not just a pricing number
* Expect Recent Data Migration runs to be smaller than the full run in most cases

**Next-Cart insight**: scope surprises usually happen when stores have complex relationships (large order history, variant-heavy catalogs, or custom data behavior). That is why a demo-first approach is often the fastest way to reduce uncertainty before committing to a final plan.

### Conclusion

Entity Points are designed to make migration scope predictable by reflecting workload and risk, not just raw counts. If you base the estimate on real admin totals, you can select a plan more confidently and avoid last-minute upgrades.

If you want to confirm scope in a practical way, running a **Demo Migration** gives you an early view of how key entities map and what needs attention in validation. When the store is more complex or you want a clearer readout, you can also request an **assisted demo** by sharing a small sample dataset so the Next-Cart team can run the demo and provide a structured results summary.

If questions come up while you are sizing scope or deciding how much help you need, **Live Chat** is the fastest way to get guidance on plan fit and whether Standard Migration, Managed Migration, or Custom Migration is the right match.

#### FAQs

<details>

<summary><strong>Do images, categories, or reviews increase Entity Points?</strong></summary>

No. Entity Points are calculated from products, orders, blog posts, and customers only.

Supporting data may still be included in scope depending on platform support, but it does not increase the Entity Points calculation.

</details>

<details>

<summary><strong>Do I need a new plan for Recent Data Migration?</strong></summary>

**Do I need a new plan for Recent Data Migration?**

Not automatically. Because the plan is per run, you only need an upgrade if a single Recent Data Migration run exceeds your current plan’s Entity Points.

Plus, you'll only be charged the difference between your existing plan and the upgraded one, so there’s no need to pay full price again.

As a bonus, your 1-year license will be extended by an additional month, ensuring you get even more value.<br>

</details>

<details>

<summary><strong>Is Next-Cart pricing a subscription?</strong></summary>

Next-Cart is a one-off payment model for your migration project, not a recurring monthly subscription.

The migration service purchase includes a 1-year license, with a 1-month extension when upgrading the Entity Points plan.

</details>
