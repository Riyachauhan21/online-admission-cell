class OnlineAdmission:
    def __init__(self):
        self.applicants = {}

    def apply_online(self, name, email, high_school_code):
        if high_school_code == "970000":
            print("You are a homeschooler. Your application is being processed.")
        else:
            print("Your high school code is being verified.")
        self.applicants[name] = {"email": email, "high_school_code": high_school_code}

    def confirm_details(self, name):
        if name in self.applicants:
            print("Your details are being confirmed.")
        else:
            print("You have not applied online yet.")

    def transfer_credits(self, name, transcripts):
        if name in self.applicants:
            print("Your transcripts are being processed.")
        else:
            print("You have not applied online yet.")

# Example usage:
admission_system = OnlineAdmission()
admission_system.apply_online("John Doe", "johndoe@example.com", "123456")
admission_system.confirm_details("John Doe")
admission_system.transfer_credits("John Doe", "transcripts.pdf")
