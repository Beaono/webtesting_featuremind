describe('My Featuremind Assignment', () => {
    it('verify-siteURL', () => {

        cy.visit("https://www.automationexercise.com/")
        cy.url().should('eq', 'https://www.automationexercise.com/')
        cy.title().should('eq', 'Automation Exercise')
    })



    it('click on the cart icon ', () => {
        cy.visit("https://www.automationexercise.com/view_cart")
        // cy.get('.shop-menu')
        cy.get('ul.nav').contains('a', 'Cart').should('have.attr', 'href', '/view_cart');
      
    })

    it('verify that the cart is empty', () => {
        cy.visit('https://www.automationexercise.com/view_cart')
        cy.get('.text-center').should('have.text', 'Cart is empty! Click here to buy products.');
    })

    it('Click on the products button', () => {
        cy.visit('https://www.automationexercise.com/products')

    })

    it('Click on T-shirt option under men category', () => {
        cy.visit('https://www.automationexercise.com/products')
        cy.get('div#Men.panel-collapse.collapse')
        .invoke('css', 'display', 'block')
        .should('be.visible').click()
        .contains('Tshirts').click();
     
    })

    it('Add 3 random products', () => {
        cy.visit('https://www.automationexercise.com/products')
        cy.get('.single-products .productinfo [data-product-id="1"]').should('have.text', 'Add to cart').click()
        cy.get('.btn-success[data-dismiss="modal"]').should('have.text', 'Continue Shopping').click()

        // Adding second product
        cy.get('.single-products .productinfo [data-product-id="2"]').should('have.text', 'Add to cart').click()
        cy.get('.btn-success[data-dismiss="modal"]').should('have.text', 'Continue Shopping').click()

        //Adding third product
        cy.get('.single-products .productinfo [data-product-id="3"]').should('have.text', 'Add to cart').click()
        cy.get('.btn-success[data-dismiss="modal"]').should('have.text', 'Continue Shopping').click()
    }) 

    it('confirming the view cart link redirects to the cart page after adding products', () => {

        cy.visit('https://www.automationexercise.com/view_cart')
        cy.url().should('eq', 'https://www.automationexercise.com/view_cart')
        
    })

    it('verify there are items in the cart and its cost', () => {
        cy.visit('https://www.automationexercise.com/view_cart')
        cy.get('#cart_items .container').should('exist');
        cy.get('#cart_info').should('exist');
        cy.get('#cart_info').should('have.length.gt', 0)

    }) 
         
       
    it('signup to proceed to checkout', () => {
        cy.visit('https://www.automationexercise.com/login')
        cy.get('[data-qa="signup-name"]').type('Ehitta')
        cy.get('[data-qa="signup-email"]').type('beahitta@gmail.com') //kindly provide a different email address while carrying out this test so it doesn't fail.
        cy.get('[data-qa="signup-button"]').click();
        cy.get('#password').type('password1')
        cy.get('#days').select(2);
        cy.get('#months').select('March');
        cy.get('#years').select('1994');
        cy.get('#first_name').type('Bea')
        cy.get('#last_name').type('Ono')
        cy.get('#company').type('Bounty')
        cy.get('#address1').type('Wilson Street')
        cy.get('#country').select(0);
        cy.get('#state').type("Prish")
        cy.get('#city').type('prishyan')
        cy.get('#zipcode').type(10002)
        cy.get('#mobile_number').type('+971 52345678')
        cy.get('[data-qa="create-account"]').click();
        cy.get('[data-qa="continue-button"]').click() 

    })

    it('login page', () => {
        cy.visit('https://www.automationexercise.com/login')
        cy.get('[data-qa="login-email"]').type('beahitta@gmail.com')
        cy.get('[data-qa="login-password"]').type('password1')
        cy.get('[data-qa="login-button"]').click()
        

    })
  
                 

       
}) 
 