# Daml Fundamentals Certificate Sample App

## Timesheets and Invoices

This is a rudimentary system for offering work to contractors, maintaining a record of their time worked, and then creating and paying invoices for that time.

There are three types of parties:
* Comptroller: This party signs off on offers of work and pays invoices
* Manager: This party also signs off on offers of work and can approve time submitted by contractors. Approved time becomes an invoice that the Comptroller can pay.
* Contractor: This party can accept or reject offers of work, submit time for approval, and view invoices pertaining to their own work.

### The Offer

The Manager and Comptroller can propose an Offer to a Contractor. All three parties can see the Offer.

The Contractor can accept or reject the Offer.

### The Service Agreement

If the Offer is accepted, a Service Agreement is created. All three parties can see the Service Agreement.

The Contractor can exercise a choice on the Service Agreement to submit additional time for approval.

The Manager can exercise a choice on the Service Agreement so approve some amount of time. When time is approved, an Invoice is created.

### The Invoice

An Invoice is created by the approval of the Manager. The Manager is thus a witness to the creation of the Invoice, but is not an observer or signatory on the Invoice contract. Therefore, the Manager cannot check on the status of an Invoice (i.e., check whether it's been paid or not).

The Invoice can be observed by the Contractor. The Comptroller is the signatory.

### Building
To compile the project
```
$ daml build
```

### Testing
To test all scripts:
Either run the pre-written script in the `Test.daml` under /daml OR run:
```
$ daml start
```

### Running
To load the project into the sandbox and start navigator:
```
$ daml start
```
