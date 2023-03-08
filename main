#include <iostream>
#include <vector>
#include <numeric>
using namespace std;

class Student {
private:
string name;
string surname;
int album_number{};
vector<float> grades;
public:
void inputation() {
    cout << "Input name: ";
    cin >> name;
    cout << "Input surname: ";
    cin >> surname;
    cout << "Input album number: ";
    album_number = validation_of_the_album();
    cout << "Input grades:\n";
    vector<float> data_grades;
    int i;
    for (i = 0; i <= 4; i++) {
        cout << "Input " << i + 1 << "-th mark " << endl;
        float j = 0;
        cin >> j;
        if (j >= 2.0 && j <= 5) {
            grades.emplace_back(j);
        }
    }
}

void storing_data(string &data_name, string &data_surname, int &data_album_number, vector<float> &data_grades) {
    name = data_name;
    surname = data_surname;
    album_number = data_album_number;
}

void display_summary() {
    cout << "Name - " << name << endl;
    cout << "Surname - " << surname << endl;
    cout << "Album number -  " << album_number << endl;
    cout << "Grades" << endl;
    for (int k = 0; k < grades.size(); k++) {
        cout << grades[k] << " ";
    }
    cout << endl;
}


void add_new_grades() {
    int g = 0;
    cout << "Enter how many grades you want to add? ";
    cin >> g;
    for (int d = 0; d < g; d++) {
        float m;
        cout << "Enter " << d + 1 << " mark:" << endl;
        cin >> m;
        if (m >= 2.0 || m <= 5.0) {
            grades.emplace_back(m);
        }
    }
}

void mean_grade() {
    float sum = 0;
    sum = accumulate(grades.begin(), grades.end(), 0.0f);
    cout << "The mean grade is " << sum / grades.size() << endl;
}

void inspection_of_2() {
    int twoes = 0;
    int l;
    for (l = 0; l <= grades.size(); l++) {
        if (l == 2.0) {
            twoes++;
        }
    }
    if (twoes < 1) {
        cout << "You haven`t passed the semester." << endl;
    } else {
        cout << " You have passed. Congratulations.";
    }
}

int validation_of_the_album() {
    int amount = 0;
    int i;
    int albnum;
    bool it = true;
    while (it) {
        cin >> albnum;
        int al = albnum;
        while (al % 10 > 0) {
            al /= 10;
            amount++;
        }
        if (amount == 5 || amount == 6) {
            it = false;
        }
        else {
            it = true;
             cout << "You must write number consisted of 5 or 6 digits";
             amount = 0;
        }
    }
    return albnum;
}
};

//2nd exercise - complex numbers
class Complex
{
float real_p;
float imag_p;

public:

Complex()
{
    real_p = 0;
    imag_p = 0;
}

Complex(float real, float imaginary)
{
    real_p = real;
    imag_p = imaginary;
}

Complex(float real)
{
    real_p = real;
    imag_p = 0;
}

void modify_num()
{
    cout << "Enter real part:" << endl;
    cin >> real_p;
    cout << "Enter imaginary part:" << endl;
    cin >> imag_p;
}

Complex add(Complex &b)
{
    Complex num;
    num.real_p = real_p;
    num.imag_p = imag_p;
    num.real_p += b.real_p;
    num.imag_p += b.imag_p;
    return num;
}

void print()
{
    if (imag_p < 0)
    {
        cout << real_p << " - " << abs(imag_p) << "i" << endl;
    }
    else if (imag_p > 0)
    {
        cout << real_p << " + " << imag_p << "i" << endl;
    }
    else
    {
        cout << real_p;
    }
}

void set_im(float num)
{
    imag_p = num;
}
};

int main()
{

        Student student;
        student.inputation();
        student.add_new_grades();
        student.display_summary();
        student.mean_grade();
        student.inspection_of_2();
        student.validation_of_the_album();

        Complex complex_a(1.0, -2.0); // creates 1-2i
        Complex complex_b(3.14); // creates 3.14

        complex_b.set_im(-5);

        Complex c = complex_a.add(complex_b);

        c.print(); // prints 4.14-7i
}
