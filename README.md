Title
=======================

## Synopsis

Creating a Yelp clone using Ruby on Rails

![yelp](./public/yelp.png)

## Technologies Used

- Ruby on Rails
- RSpec
- Capybara

## Job List

- [x] Not logged in users can see all the reviews
- [x] Only logged in users can add restaurants
- [x] User can log in with Facebook
- [x] Only logged in users can leave a review

## Favourite Code Snippet

~~~
def self.from_omniauth(auth)
 where(provider: auth.provider, uid: auth.uid).first_or_create do |user|
   user.email = auth.info.email
   user.password = Devise.friendly_token[0, 20]
 end
end
~~~

## Collaborators

- [Steph Oldcorn](http://www.github.com/stepholdcorn)
- [Matteo Manzo](http://www.github.com/matteomanzo)

## Still to complete/refactor

- [ ] Adding images to restaurants
- [ ] User can only post one review per restaurant
- [ ] CSS styling

## Takeaway

Convention over configuration, the essence of a very powerful framework as Ruby on Rails
