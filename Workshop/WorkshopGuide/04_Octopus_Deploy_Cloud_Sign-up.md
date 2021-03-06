# NDCDevOpsWorkshop Octopus Cloud Sign-up

## Octopus Cloud Sign-up

This section will be instructor-led, but full details should be below. 

You will need to sign-up for the free Cloud edition for each attendee. You can get more details on [Octopus.com](https://octopus.com/start).

- Browse to <https://octopus.com/start>
- Select Cloud
- Input URL, Select the **Australia** Region, Company Name, and Phone number
- Press "Agree, start my trial"
- Wait for it to spin up & sign in.
- Take note of the URL

## Teams Setup

In this section, we will create two teams, one called **Infrastructure** and one called **Build Servers**.

These teams will have embedded service accounts so we can use them to pass the artifacts generated by Github Actions, provision infrastructure in Azure, and register them via the Octopus API. 

### Infrastructure Team

If the team doesn't exist, please proceed with the below: 

- Logon to your Octopus Instance
- Browse to Configuration -> Teams
- Select **Add Team**
- Input the name of **Infrastructure**, add a suitable description, and make it only applicable to the local space. 
- It will now create the team. 
- Browse to **User Roles** and select **Include User Role**
- Add **Environment Manager** and **Space Manager** permissions to the team, and select save

### Build Team

If the team doesn't exist, please proceed with the below: 

- Logon to your Octopus Instance
- Browse to Configuration -> Teams
- Select **Add Team**
- Input the name of **Build Servers**, add a suitable description, and make it only applicable to the local space. 
- It will now create the team. 
- Browse to **User Roles** and select **Include User Role**
- Add **Build Server** and **Deployment Creator** and **Release Creator** permissions to the team, and select save

## Accounts

In this section, we will create two Service accounts, one called **SVC-GHA** and one called **SVC-INFRASTRUCTURE**, and add these users to their respective teams.

### Github Service Account Setup

- Logon to your Octopus Instance
- Browse to Configuration -> Users
- Select **Create Service Account**
- Name it **SVC-GHA**, add in a suitable display name and ensure the user has the check box ticked for **The user is a service account**
- You can now browse to Teams, Select the **Build Server** team, add the service account to the team, and hit save. 
- Generate the API key, and store this in a secure location. 

### Infrastructure Service Account Setup

- Logon to your Octopus Instance
- Browse to Configuration -> Users
- Select **Create Service Account**
- Name it **SVC-Infrastructure**, add in a suitable display name and ensure the user has the check box ticked for **The user is a service account**
- You can now browse to Teams, Select the **Infrastructure** team, add the service account to the team, and hit save. 
- Generate the API key, and store this in a secure location.

## Next Sction

[Azure-Sign-up](05_Azure_Sign-up.md)