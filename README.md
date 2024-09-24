#include <iostream>
#include <string>
#include <vector>

class UserDetails {
public:
     User Information
    std::string name = "Sunil Kumar";
    std::string location = "Bangalore, Karnataka";
    std::string email = "sunilkumar1247@outlook.com";
    std::string phone = "+91 8867776875";
    
     Education Details
    struct Education {
        std::string degree;
        std::string institution;
        std::string grade;
        std::string location;
        std::string startDate;
        std::string endDate;
    };
    
    Education bca = {"Bachelor of Computer Applications", "Himalayan Garhwal University", "CGPA - 70", "Uttarakhand, India", "June 2019", "August 2021"};
    Education intermediate = {"Intermediate", "Narayana Junior College", "67%", "Kadapa, India", "March 2016", "July 2018"};
    
     Skills
    std::vector<std::string> skills = {
        "C++", "SQL", "Data Structures & Algorithms", 
        "Operating Systems", "Computer Networks", 
        "Low Level System Design", "High Level System Design"
    };
    
     Projects
    struct Project {
        std::string title;
        std::vector<std::string> technologies;
        std::string description;
    };

    std::vector<Project> projects = {
        {
            "Distributed Key-Value Store", 
            {"C++", "SQL", "Networking", "Consistent Hashing"},
            "Designed a distributed key-value store using consistent hashing ensuring 99.9% availability."
        },
        {
            "In-Memory SQL Database", 
            {"C++", "SQL", "Data Structures", "Memory Management"},
            "Built an in-memory SQL database reducing query response time by 70%."
        },
        {
            "Microservices E-Commerce Platform", 
            {"C++", "SQL", "Microservices Architecture"},
            "Developed a microservices-based e-commerce platform improving scalability by 200%."
        },
        {
            "Multithreaded Web Crawler", 
            {"C++", "Multithreading", "Networking", "Data Processing"},
            "Built a multithreaded web crawler that processes 1 million web pages in 24 hours."
        }
    };
    
     Fresher status
    bool isFresher = true;

     Display Details
    void displayUserDetails() {
        std::cout << "Name: " << name << "\nLocation: " << location << "\nEmail: " << email << "\nPhone: " << phone << "\n";
        std::cout << "\nEducation:\n";
        std::cout << bca.degree << " from " << bca.institution << " (" << bca.grade << ") - " << bca.location << " (" << bca.startDate << " to " << bca.endDate << ")\n";
        std::cout << intermediate.degree << " from " << intermediate.institution << " (" << intermediate.grade << ") - " << intermediate.location << " (" << intermediate.startDate << " to " << intermediate.endDate << ")\n";
        
        std::cout << "\nSkills:\n";
        for (const auto& skill : skills) {
            std::cout << "- " << skill << "\n";
        }
        
        std::cout << "\nProjects:\n";
        for (const auto& project : projects) {
            std::cout << project.title << " (" << project.technologies[0] << "): " << project.description << "\n";
        }
        
        std::cout << "\nStatus: " << (isFresher ? "Fresher" : "Experienced") << "\n";
    }
};

int main() {
    UserDetails user;
    user.displayUserDetails();
    return 0;
}
