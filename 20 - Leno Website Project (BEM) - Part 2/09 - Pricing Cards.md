# Pricing Cards

In this section, we'll add pricing cards to the inner details page. These cards will display different pricing options for the product or service being offered.

## HTML

Let's add the html for the pricing cards on the inner details page:

```html
<!-- Pricing -->
<section class="pricing">
  <div class="pricing__container container">
    <h2 class="pricing__title">Pricing Options</h2>
    <div class="pricing__cards">
      <div class="pricing__card">
        <div class="pricing__card-box">
          <h4 class="pricing__card-title">Standard</h4>
          <h3 class="pricing__card-price">Free</h3>
          <div class="pricing__card-body">
            <ul class="pricing__card-list">
              <li class="pricing__card-item">
                <i class="fas fa-check"></i> Unlimited access to all features
              </li>
              <li class="pricing__card-item">
                <i class="fas fa-check"></i> 24/7 customer support
              </li>
              <li class="pricing__card-item">
                <i class="fas fa-check"></i> 1GB storage
              </li>
              <li class="pricing__card-item">
                <i class="fas fa-check"></i> Cancel anytime
              </li>
            </ul>
          </div>
        </div>
        <a href="#" class="pricing__card-button button">Get Started</a>
      </div>
      <div class="pricing__card">
        <div class="pricing__card-box">
          <h4 class="pricing__card-title">Advanced</h4>
          <h3 class="pricing__card-price">$19</h3>
          <div class="pricing__card-body">
            <ul class="pricing__card-list">
              <li class="pricing__card-item">
                <i class="fas fa-check"></i> Unlimited access to all features
              </li>
              <li class="pricing__card-item">
                <i class="fas fa-check"></i> 24/7 customer support
              </li>
              <li class="pricing__card-item">
                <i class="fas fa-check"></i> 3GB storage
              </li>
              <li class="pricing__card-item">
                <i class="fas fa-check"></i> Cancel anytime
              </li>
            </ul>
          </div>
        </div>
        <a href="#" class="pricing__card-button button">Get Started</a>
      </div>
      <div class="pricing__card">
        <div class="pricing__card-box">
          <h4 class="pricing__card-title">Complete</h4>
          <h3 class="pricing__card-price">$29</h3>
          <div class="pricing__card-body">
            <ul class="pricing__card-list">
              <li class="pricing__card-item">
                <i class="fas fa-check"></i> Unlimited access to all features
              </li>
              <li class="pricing__card-item">
                <i class="fas fa-check"></i> 24/7 customer support
              </li>
              <li class="pricing__card-item">
                <i class="fas fa-check"></i> 10GB storage
              </li>
              <li class="pricing__card-item">
                <i class="fas fa-check"></i>Cancel anytime
              </li>
            </ul>
          </div>
        </div>
        <a href="#" class="pricing__card-button button">Get Started</a>
      </div>
    </div>
  </div>
</section>
```

Each card has a title, price, and list of features. The features are displayed as a list of items with a checkmark icon. Each card also has a "Get Started" button.

The cards are contained within a `pricing__cards` div, which is a flex container that arranges the cards in a row.

## CSS

Now let's add the CSS for the pricing section:

```css
/* Pricing */
.pricing {
  padding: 4rem 2rem 6rem;
  background: var(--tertiary-color);
}

.pricing__title {
  font-size: 2.3rem;
  margin-bottom: 2rem;
  text-transform: uppercase;
  text-align: center;
}

.pricing__cards {
  display: flex;
  justify-content: space-between;
  align-items: center;
  text-align: center;
  gap: 2rem;
}

.pricing__card-box {
  padding: 2.5rem;
  background: rgba(255, 255, 255, 0.1);
  margin-bottom: 2rem;
  border-radius: 30px;
}

.pricing__card-title {
  font-size: 1.4rem;
  text-transform: uppercase;
}

.pricing__card-price {
  font-size: 3rem;
  font-weight: 700;
  color: var(--primary-color);
  margin-bottom: 1rem;
}

.pricing__card-list {
  text-align: left;
  line-height: 2.5rem;
  font-weight: 300;
}

.pricing__card-item i {
  color: var(--primary-color);
  margin-right: 0.5rem;
}
```

They should look like this:

<img src="../images/leno-pricing.png" />

They look good, but they are not responsive yet. Let's add some CSS in the `768px` media query to make them responsive:

```css
/* Pricing */
.pricing__cards {
  flex-direction: column;
}

.pricing__card-box {
  margin-bottom: 4.5rem;
}
```

We are just changing the layout from a row to a column on smaller screens and adding some margin between the cards.

## Pricing Notes

Let's add the pricing notes section under the pricing cards:

```html
<!-- Pricing Notes -->
<section class="pricing-notes">
  <div class="pricing-notes__container container">
    <p class="pricing-notes__text">
      * At varius vel pharetra vel turpis nunc eget lorem dolor. Tincidunt nunc
      pulvinar sapien et ligula brizo simpa
    </p>
    <p class="pricing-notes__text">
      ** Feugiat in fermentum posuere urna nec tincidunt praesent. Tempus
      egestas sed sed risus pretium reno vinto licra
    </p>
    <p class="pricing-notes__text">
      *** Adipiscing elit duis tristique sollicitudin nibh. Non consectetur a
      erat nam at lectus ventum sinop loma nipo vifor
    </p>
  </div>
</section>
```

A little bit of CSS:

```css
/* Pricing Notes */
.pricing-notes {
  padding: 3rem 2rem;
  color: #9f9caf;
  text-align: center;
}
```
