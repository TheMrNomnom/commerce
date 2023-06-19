# commerce

This is a Django web application for online auctions. Users can create listings, place bids on listings, add listings to their watchlist, and comment on listings.

## Installation

1. Clone the repository:

```
git clone https://github.com/TheMrNomnom/commerce.git
```

2. Navigate to the project directory:

```
cd commerce
```

3. Install the required dependencies:

```
pip install django && pip install requests
```

4. Apply database migrations:

```
python manage.py migrate
```

5. Start the development server:

```
python manage.py runserver
```

6. Access the application in your web browser at `http://localhost:8000`.

## Usage

- Home Page (`/`): Displays all active listings and listings where the user is the creator or winner.
- Login (`/login`): Allows users to log in to their accounts.
- Logout (`/logout`): Logs out the current user.
- Register (`/register`): Allows new users to create an account.
- Categories (`/categories`): Displays all available categories.
- Watchlist (`/watchlist`): Shows listings added to the user's watchlist.
- Create Listing (`/create_listing`): Allows authenticated users to create a new listing.
- Category Listings (`/category/<int:category_id>`): Displays listings filtered by the selected category.
- Listing View (`/listing/<int:listing_id>`): Displays detailed information about a specific listing, including bids and comments.

## Dependencies

The application uses the following dependencies:

- [Django](https://www.djangoproject.com/): A high-level Python web framework.
- [Requests](https://pypi.org/project/requests/): A Python library for making HTTP requests.
- [Bootstrap](https://getbootstrap.com/): A popular CSS framework for building responsive and mobile-first websites.


## HTML Templates

The following HTML templates are used in the application:

- `categories.html`: Displays a list of categories for the auctions.
- `create_listing.html`: Allows users to create a new listing by filling out a form.
- `index.html`: Shows a list of active listings.
- `layout.html`: Defines the layout structure for all other templates and includes common elements like navigation, authentication status, and messages.
- `listing.html`: Displays the details of a specific listing, including the current highest bid and comments.
- `watchlist.html`: Shows the listings that the user has added to their watchlist.
- `register.html`: Provides a registration form for new users to create an account.
- `login.html`: Displays a login form for existing users to log in to their accounts.


## Models

The application defines the following models:

- `User`: Represents a user account and extends the Django `AbstractUser` model.
- `Category`: Represents a category for listings.
- `Listing`: Represents a listing with title, description, image URL, creator, category, status, and winner.
- `Bid`: Represents a bid on a listing with an amount, listing reference, and user reference.
- `Comment`: Represents a comment on a listing with text, listing reference, user reference, and date-time.

## Contributing

Contributions are welcome! If you find any issues or want to enhance the application, feel free to submit a pull request.

Please ensure that your code follows the PEP 8 style guide and includes appropriate tests.

## Credits

This project is developed based on the specifications provided by [CS50](https://cs50.harvard.edu/web/2020/projects/2/commerce/) from Harvard University.

## License

This project is licensed under the MIT License. You can find the license information in the [LICENSE](LICENSE) file.
