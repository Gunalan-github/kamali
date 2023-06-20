# LONG CODING
import java.util.ArrayList;
import java.util.List;
import java.util.Scanner;

class User {
    private String username;
    private String password;
    private String email;
    // Additional user profile information
    
    public User(String username, String password, String email) {
        this.username = username;
        this.password = password;
        this.email = email;
    }
    
    // Getters and setters for user profile fields
    
    public String getUsername() {
        return username;
    }
    
    public String getPassword() {
        return password;
    }
    
    public String getEmail() {
        return email;
    }
}

class Movie {
    private String title;
    private String description;
    private double rating;
    // Additional movie information
    
    public Movie(String title, String description, double rating) {
        this.title = title;
        this.description = description;
        this.rating = rating;
    }
    
    // Getters and setters for movie fields
    
    public String getTitle() {
        return title;
    }
    
    public String getDescription() {
        return description;
    }
    
    public double getRating() {
        return rating;
    }
}

class Booking {
    private User user;
    private Movie movie;
    private String showtime;
    private List<String> selectedSeats;
    // Additional booking information
    
    public Booking(User user, Movie movie, String showtime, List<String> selectedSeats) {
        this.user = user;
        this.movie = movie;
        this.showtime = showtime;
        this.selectedSeats = selectedSeats;
    }
    
    // Getters and setters for booking fields
    
    public User getUser() {
        return user;
    }
    
    public Movie getMovie() {
        return movie;
    }
    
    public String getShowtime() {
        return showtime;
    }
    
    public List<String> getSelectedSeats() {
        return selectedSeats;
    }
}

class MovieTicketBookingApp {
    private List<User> users;
    private List<Movie> movies;
    private List<Booking> bookings;
    
    public MovieTicketBookingApp() {
        users = new ArrayList<>();
        movies = new ArrayList<>();
        bookings = new ArrayList<>();
    }
    
    public void registerUser(String username, String password, String email) {
        User user = new User(username, password, email);
        users.add(user);
        System.out.println("User registered successfully!");
    }
    
    public void addMovie(String title, String description, double rating) {
        Movie movie = new Movie(title, description, rating);
        movies.add(movie);
        System.out.println("Movie added successfully!");
    }
    
    public void bookTicket(User user, Movie movie, String showtime, List<String> selectedSeats) {
        Booking booking = new Booking(user, movie, showtime, selectedSeats);
        bookings.add(booking);
        System.out.println("Ticket booked successfully!");
    }
    
    // Additional methods for viewing movie listings, payment options, movie ratings and reviews, and booking history
    
    public void viewMovieListings() {
        System.out.println("Movie Listings:");
        for (Movie movie : movies) {
            System.out.println(movie.getTitle());
        }
    }
    
    // Additional methods for payment options, movie ratings and reviews, and booking history
    
    public static void main(String[] args) {
        MovieTicketBookingApp app = new MovieTicketBookingApp();
        
        // Example usage
        
        app.registerUser("john123", "password123", "john@example.com");
        app.registerUser("emma
        // Registering users
        app.registerUser("john123", "password123", "john@example.com");
        app.registerUser("emma456", "password456", "emma@example.com");

        // Adding movies
        app.addMovie("Inception", "A mind-bending sci-fi thriller", 8.7);
        app.addMovie("The Shawshank Redemption", "A gripping tale of hope and redemption", 9.3);
        app.addMovie("The Dark Knight", "A superhero film exploring themes of chaos and morality", 9.0);

        // Viewing movie listings
        app.viewMovieListings();

        // Booking tickets
        User user = app.users.get(0);
        Movie movie = app.movies.get(0);
        List<String> selectedSeats = new ArrayList<>();
        selectedSeats.add("A1");
        selectedSeats.add("A2");
        app.bookTicket(user, movie, "June 20, 2023, 19:00", selectedSeats);

        // Additional usage for payment options, movie ratings and reviews, and booking history
        // Implement these methods based on your desired functionality

    }
}
