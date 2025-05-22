# Project Responsive Web Design using Bootstrap
## Date:

## AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.


## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

### Step 5:
Create a HTML file and include the needed Bootstrap components.

### Step 6:
Publish the website in the LocalHost.

## PROGRAM :

    ```
    <!DOCTYPE html>
    <html lang="en">
    <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dribbble Clone - Discover Design</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        :root {
            --dribbble-pink: #ea4c89;
            --dribbble-dark: #1a1a1a;
        }
        
        body {
            font-family: 'Helvetica Neue', sans-serif;
        }
        
        .navbar-brand {
            font-weight: bold;
            font-size: 1.5rem;
            color: var(--dribbble-pink) !important;
        }
        
        .btn-dribbble {
            background-color: var(--dribbble-pink);
            border-color: var(--dribbble-pink);
            color: white;
            border-radius: 25px;
            padding: 8px 20px;
            font-weight: 500;
        }
        
        .btn-dribbble:hover {
            background-color: #d63384;
            border-color: #d63384;
            color: white;
        }
        
        .hero-section {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 100px 0;
        }
        
        .shot-card {
            border: none;
            border-radius: 15px;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            margin-bottom: 30px;
        }
        
        .shot-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
        }
        
        .shot-image {
            height: 250px;
            background-size: cover;
            background-position: center;
            position: relative;
        }
        
        .shot-overlay {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(234, 76, 137, 0.9);
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .shot-card:hover .shot-overlay {
            opacity: 1;
        }
        
        .shot-stats {
            color: white;
            font-size: 1.1rem;
        }
        
        .designer-avatar {
            width: 40px;
            height: 40px;
            border-radius: 50%;
            object-fit: cover;
        }
        
        .stats-section {
            background-color: #f8f9fa;
            padding: 80px 0;
        }
        
        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: var(--dribbble-pink);
        }
        
        footer {
            background-color: var(--dribbble-dark);
            color: white;
            padding: 60px 0 30px 0;
        }
        
        .footer-link {
            color: #adb5bd;
            text-decoration: none;
            transition: color 0.3s ease;
        }
        
        .footer-link:hover {
            color: var(--dribbble-pink);
        }
        
        .social-icon {
            font-size: 1.5rem;
            margin: 0 10px;
            color: #adb5bd;
            transition: color 0.3s ease;
        }
        
        .social-icon:hover {
            color: var(--dribbble-pink);
        }
        
        @media (max-width: 768px) {
            .hero-section {
                padding: 60px 0;
            }
            
            .hero-section h1 {
                font-size: 2rem;
            }
            
            .shot-image {
                height: 200px;
            }
        }
    </style>
    </head>
    <body>
    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg navbar-light bg-white sticky-top shadow-sm">
        <div class="container">
            <a class="navbar-brand" href="#">
                <i class="fas fa-basketball-ball me-2"></i>Dribbble
            </a>
            
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav me-auto">
                    <li class="nav-item">
                        <a class="nav-link" href="#shots">Shots</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#designers">Designers</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#teams">Teams</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#community">Community</a>
                    </li>
                </ul>
                
                <div class="d-flex">
                    <input class="form-control me-2" type="search" placeholder="Search..." style="width: 200px;">
                    <button class="btn btn-outline-secondary me-2">Sign in</button>
                    <button class="btn btn-dribbble">Sign up</button>
                </div>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero-section">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-6">
                    <h1 class="display-4 fw-bold mb-4">Discover the world's top designers & creatives</h1>
                    <p class="lead mb-4">Dribbble is the leading destination to find & showcase creative work and home to the world's best design professionals.</p>
                    <button class="btn btn-light btn-lg me-3">Sign up</button>
                    <button class="btn btn-outline-light btn-lg">Learn more</button>
                </div>
                <div class="col-lg-6 text-center">
                    <img src="https://ik.imagekit.io/0tydz7atd/Screenshot%202025-05-22%20081827.png?updatedAt=1747882164863" alt="Hero Image" class="img-fluid rounded-3">
                </div>
            </div>
        </div>
    </section>

    <!-- Featured Shots -->
    <section class="py-5" id="shots">
        <div class="container">
            <div class="row mb-5">
                <div class="col-12 text-center">
                    <h2 class="display-5 fw-bold mb-3">Popular shots</h2>
                    <p class="text-muted">Explore trending designs from the community</p>
                </div>
            </div>
            
            <div class="row">
                <div class="col-lg-3 col-md-6 mb-4">
                    <div class="card shot-card">
                        <div class="shot-image" style="background-image: url('https://ik.imagekit.io/0tydz7atd/images%20(2).jpeg?updatedAt=1747882905078');">
                            <div class="shot-overlay">
                                <div class="shot-stats">
                                    <i class="far fa-heart me-2"></i>124
                                    <i class="far fa-eye ms-3 me-2"></i>2.1k
                                </div>
                            </div>
                        </div>
                        <div class="card-body">
                            <div class="d-flex align-items-center">
                                <img src="https://ik.imagekit.io/0tydz7atd/images%20(1).jpeg?updatedAt=1747882817528" alt="Designer" class="designer-avatar me-3">
                                <div>
                                    <h6 class="mb-0">Sarah Johnson</h6>
                                    <small class="text-muted">UI/UX Designer</small>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="col-lg-3 col-md-6 mb-4">
                    <div class="card shot-card">
                        <div class="shot-image" style="background-image: url('https://ik.imagekit.io/0tydz7atd/8a8f69106249811.Y3JvcCw2OTk5LDU0NzUsMCww.jpg?updatedAt=1747883108646');">
                            <div class="shot-overlay">
                                <div class="shot-stats">
                                    <i class="far fa-heart me-2"></i>89
                                    <i class="far fa-eye ms-3 me-2"></i>1.5k
                                </div>
                            </div>
                        </div>
                        <div class="card-body">
                            <div class="d-flex align-items-center">
                                <img src="https://ik.imagekit.io/0tydz7atd/images.jpeg?updatedAt=1747883035646" alt="Designer" class="designer-avatar me-3">
                                <div>
                                    <h6 class="mb-0">Mike Chen</h6>
                                    <small class="text-muted">Brand Designer</small>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="col-lg-3 col-md-6 mb-4">
                    <div class="card shot-card">
                        <div class="shot-image" style="background-image: url('https://ik.imagekit.io/0tydz7atd/raf,360x360,075,t,fafafa_ca443f4786.jpg?updatedAt=1747883364478');">
                            <div class="shot-overlay">
                                <div class="shot-stats">
                                    <i class="far fa-heart me-2"></i>156
                                    <i class="far fa-eye ms-3 me-2"></i>3.2k
                                </div>
                            </div>
                        </div>
                        <div class="card-body">
                            <div class="d-flex align-items-center">
                                <img src="https://ik.imagekit.io/0tydz7atd/EmilyRodriguez_1-23-25_MargotMurphy-e1737748629702-1200x1113.jpg?updatedAt=1747883224610" alt="Designer" class="designer-avatar me-3">
                                <div>
                                    <h6 class="mb-0">Emily Rodriguez</h6>
                                    <small class="text-muted">Illustrator</small>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="col-lg-3 col-md-6 mb-4">
                    <div class="card shot-card">
                        <div class="shot-image" style="background-image: url('https://ik.imagekit.io/0tydz7atd/letter-w-modern-technological-logo_575535-180.avif?updatedAt=1747883459289');">
                            <div class="shot-overlay">
                                <div class="shot-stats">
                                    <i class="far fa-heart me-2"></i>203
                                    <i class="far fa-eye ms-3 me-2"></i>4.1k
                                </div>
                            </div>
                        </div>
                        <div class="card-body">
                            <div class="d-flex align-items-center">
                                <img src="https://ik.imagekit.io/0tydz7atd/RR_AlexThompson_colorcutout-800x627.webp?updatedAt=1747883499535" alt="Designer" class="designer-avatar me-3">
                                <div>
                                    <h6 class="mb-0">Alex Thompson</h6>
                                    <small class="text-muted">Web Designer</small>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            
            
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="row">
                <div class="col-lg-3 col-md-6 mb-4">
                    <h5 class="mb-3">For designers</h5>
                    <ul class="list-unstyled">
                        <li><a href="#" class="footer-link">Go Pro!</a></li>
                        <li><a href="#" class="footer-link">Explore design work</a></li>
                        <li><a href="#" class="footer-link">Design blog</a></li>
                        <li><a href="#" class="footer-link">Overtime podcast</a></li>
                        <li><a href="#" class="footer-link">Playoffs</a></li>
                    </ul>
                </div>
                
                <div class="col-lg-3 col-md-6 mb-4">
                    <h5 class="mb-3">Hire designers</h5>
                    <ul class="list-unstyled">
                        <li><a href="#" class="footer-link">Post a job opening</a></li>
                        <li><a href="#" class="footer-link">Post a freelance project</a></li>
                        <li><a href="#" class="footer-link">Search for designers</a></li>
                        <li><a href="#" class="footer-link">Brands</a></li>
                        <li><a href="#" class="footer-link">Advertise with us</a></li>
                    </ul>
                </div>
                
                <div class="col-lg-3 col-md-6 mb-4">
                    <h5 class="mb-3">Company</h5>
                    <ul class="list-unstyled">
                        <li><a href="#" class="footer-link">About</a></li>
                        <li><a href="#" class="footer-link">Careers</a></li>
                        <li><a href="#" class="footer-link">Support</a></li>
                        <li><a href="#" class="footer-link">Media kit</a></li>
                        <li><a href="#" class="footer-link">Testimonials</a></li>
                    </ul>
                </div>
                
                <div class="col-lg-3 col-md-6 mb-4">
                    <h5 class="mb-3">Directories</h5>
                    <ul class="list-unstyled">
                        <li><a href="#" class="footer-link">Design jobs</a></li>
                        <li><a href="#" class="footer-link">Designers for hire</a></li>
                        <li><a href="#" class="footer-link">Freelance designers</a></li>
                        <li><a href="#" class="footer-link">Tags</a></li>
                        <li><a href="#" class="footer-link">Places</a></li>
                    </ul>
                </div>
            </div>
            
            <hr class="my-4" style="border-color: #495057;">
            
            <div class="row align-items-center">
                <div class="col-md-6">
                    <p class="mb-0">&copy; 2025 Dribbble. All rights reserved.</p>
                </div>
                <div class="col-md-6 text-md-end">
                    <a href="#" class="social-icon"><i class="fab fa-twitter"></i></a>
                    <a href="#" class="social-icon"><i class="fab fa-facebook"></i></a>
                    <a href="#" class="social-icon"><i class="fab fa-instagram"></i></a>
                    <a href="#" class="social-icon"><i class="fab fa-pinterest"></i></a>
                </div>
            </div>
        </div>
    </footer>

    

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    </body>
    </html>

    ```

## OUTPUT:

![image](https://github.com/user-attachments/assets/e1ba3490-b7ef-4fc3-be9e-a3516bbe6533)



## RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
