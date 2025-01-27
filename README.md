```graphql
schema-codegen-start
const typeDefs = `
  type Credit_Union {
    id: ID!
    Contract_Number: String!
    Credit_Union_Name: String!
    Premium_Reports: [Premium_Report]
    Premium_Adjustments: [Premium_Adjustment]
    Single_Premium_Certificate_Returns: [Single_Premium_Certificate_Return]
  }

  type Premium_Report {
    id: ID!
    Product_Name: String!
    Report_Period: String!
    Status: String!
    Last_Update: String!
    Period_Ending: String!
    Adjustment_Type_to_the_Credit_Union: String!
    Comment: String!
    Total_Borrower_Fees_: Float!
    CU_Retail_Rate: Float!
    Protected_Loan_Amount: Float!
    Pay_Rate: Float!
    Premium_Due: Float!
    Total_Amount: Float!
  }

  type Premium_Adjustment {
    id: ID!
    Product_Name: String!
    Report_Period: String!
    Status: String!
    Last_Update: String!
    Period_Ending: String!
    Adjustment_Type_to_the_Credit_Union: String!
    Comment: String!
    Total_Borrower_Fees_: Float!
    CU_Retail_Rate: Float!
    Protected_Loan_Amount: Float!
    Pay_Rate: Float!
    Premium_Due: Float!
    Total_Amount: Float!
  }

  type Single_Premium_Certificate_Return {
    id: ID!
  }

  input Credit_Union_Input {
    id: ID
    Contract_Number: String!
    Credit_Union_Name: String!
  }

  input Premium_Report_Input {
    id: ID
    Product_Name: String!
    Report_Period: String!
    Status: String!
    Last_Update: String!
    Period_Ending: String!
    Adjustment_Type_to_the_Credit_Union: String!
    Comment: String!
    Total_Borrower_Fees_: Float!
    CU_Retail_Rate: Float!
    Protected_Loan_Amount: Float!
    Pay_Rate: Float!
    Premium_Due: Float!
    Total_Amount: Float!
  }

  input Premium_Adjustment_Input {
    id: ID
    Product_Name: String!
    Report_Period: String!
    Status: String!
    Last_Update: String!
    Period_Ending: String!
    Adjustment_Type_to_the_Credit_Union: String!
    Comment: String!
    Total_Borrower_Fees_: Float!
    CU_Retail_Rate: Float!
    Protected_Loan_Amount: Float!
    Pay_Rate: Float!
    Premium_Due: Float!
    Total_Amount: Float!
  }

  input Single_Premium_Certificate_Return_Input {
    id: ID
  }

  type Query {
    getCreditUnion(id: ID!): Credit_Union
    listCreditUnions: [Credit_Union]
    getPremiumReport(id: ID!): Premium_Report
    listPremiumReports: [Premium_Report]
    getPremiumAdjustment(id: ID!): Premium_Adjustment
    listPremiumAdjustments: [Premium_Adjustment]
    getSinglePremiumCertificateReturn(id: ID!): Single_Premium_Certificate_Return
    listSinglePremiumCertificateReturns: [Single_Premium_Certificate_Return]
  }

  type Mutation {
    addCreditUnion(input: Credit_Union_Input!): Credit_Union
    updateCreditUnion(id: ID!, input: Credit_Union_Input!): Credit_Union
    deleteCreditUnion(id: ID!): Credit_Union
    addPremiumReport(input: Premium_Report_Input!): Premium_Report
    updatePremiumReport(id: ID!, input: Premium_Report_Input!): Premium_Report
    deletePremiumReport(id: ID!): Premium_Report
    addPremiumAdjustment(input: Premium_Adjustment_Input!): Premium_Adjustment
    updatePremiumAdjustment(id: ID!, input: Premium_Adjustment_Input!): Premium_Adjustment
    deletePremiumAdjustment(id: ID!): Premium_Adjustment
    addSinglePremiumCertificateReturn(input: Single_Premium_Certificate_Return_Input!): Single_Premium_Certificate_Return
    updateSinglePremiumCertificateReturn(id: ID!, input: Single_Premium_Certificate_Return_Input!): Single_Premium_Certificate_Return
    deleteSinglePremiumCertificateReturn(id: ID!): Single_Premium_Certificate_Return
  }
`;
schema-codegen-end
```

```javascript
resolver-codegen-start
const resolvers = {
  Query: {
    getCreditUnion: (_, { id }) => {
      // Placeholder: return a sample credit union or fetch from database
      return {
        id,
        Contract_Number: "CN123",
        Credit_Union_Name: "Sample CU",
        Premium_Reports: [],
        Premium_Adjustments: [],
        Single_Premium_Certificate_Returns: [],
      };
    },
    listCreditUnions: () => {
      // Placeholder: return a list of sample credit unions
      return [
        {
          id: "1",
          Contract_Number: "CN123",
          Credit_Union_Name: "Sample CU",
          Premium_Reports: [],
          Premium_Adjustments: [],
          Single_Premium_Certificate_Returns: [],
        },
      ];
    },
    getPremiumReport: (_, { id }) => {
      // Placeholder: return a sample premium report or fetch from database
      return {
        id,
        Product_Name: "Sample Product",
        Report_Period: "2021 Q1",
        Status: "Active",
        Last_Update: "2021-04-01",
        Period_Ending: "2021-03-31",
        Adjustment_Type_to_the_Credit_Union: "Adjustment A",
        Comment: "Monthly report",
        Total_Borrower_Fees_: 100.5,
        CU_Retail_Rate: 1.5,
        Protected_Loan_Amount: 10000,
        Pay_Rate: 1.2,
        Premium_Due: 150,
        Total_Amount: 1050,
      };
    },
    listPremiumReports: () => {
      // Placeholder: return a list of sample premium reports
      return [
        {
          id: "1",
          Product_Name: "Sample Product",
          Report_Period: "2021 Q1",
          Status: "Active",
          Last_Update: "2021-04-01",
          Period_Ending: "2021-03-31",
          Adjustment_Type_to_the_Credit_Union: "Adjustment A",
          Comment: "Monthly report",
          Total_Borrower_Fees_: 100.5,
          CU_Retail_Rate: 1.5,
          Protected_Loan_Amount: 10000,
          Pay_Rate: 1.2,
          Premium_Due: 150,
          Total_Amount: 1050,
        },
      ];
    },
    getPremiumAdjustment: (_, { id }) => {
      // Placeholder: return a sample premium adjustment or fetch from database
      return {
        id,
        Product_Name: "Sample Product",
        Report_Period: "2021 Q1",
        Status: "Active",
        Last_Update: "2021-04-01",
        Period_Ending: "2021-03-31",
        Adjustment_Type_to_the_Credit_Union: "Adjustment A",
        Comment: "Monthly adjustment",
        Total_Borrower_Fees_: 100.5,
        CU_Retail_Rate: 1.5,
        Protected_Loan_Amount: 10000,
        Pay_Rate: 1.2,
        Premium_Due: 150,
        Total_Amount: 1050,
      };
    },
    listPremiumAdjustments: () => {
      // Placeholder: return a list of sample premium adjustments
      return [
        {
          id: "1",
          Product_Name: "Sample Product",
          Report_Period: "2021 Q1",
          Status: "Active",
          Last_Update: "2021-04-01",
          Period_Ending: "2021-03-31",
          Adjustment_Type_to_the_Credit_Union: "Adjustment A",
          Comment: "Monthly adjustment",
          Total_Borrower_Fees_: 100.5,
          CU_Retail_Rate: 1.5,
          Protected_Loan_Amount: 10000,
          Pay_Rate: 1.2,
          Premium_Due: 150,
          Total_Amount: 1050,
        },
      ];
    },
    getSinglePremiumCertificateReturn: (_, { id }) => {
      // Placeholder: return a sample single premium certificate return or fetch from database
      return { id };
    },
    listSinglePremiumCertificateReturns: () => {
      // Placeholder: return a list of sample single premium certificate returns
      return [{ id: "1" }];
    },
  },
  Mutation: {
    addCreditUnion: (_, { input }) => {
      // Placeholder: add a credit union to the database and return it
      return { id: "1", ...input, Premium_Reports: [], Premium_Adjustments: [], Single_Premium_Certificate_Returns: [] };
    },
    updateCreditUnion: (_, { id, input }) => {
      // Placeholder: update a credit union in the database and return it
      return { id, ...input, Premium_Reports: [], Premium_Adjustments: [], Single_Premium_Certificate_Returns: [] };
    },
    deleteCreditUnion: (_, { id }) => {
      // Placeholder: delete a credit union from the database and confirm the deletion
      return { id, Contract_Number: "Deleted", Credit_Union_Name: "Deleted", Premium_Reports: [], Premium_Adjustments: [], Single_Premium_Certificate_Returns: [] };
    },
    addPremiumReport: (_, { input }) => {
      // Placeholder: add a premium report to the database and return it
      return { id: "1", ...input };
    },
    updatePremiumReport: (_, { id, input }) => {
      // Placeholder: update a premium report in the database and return it
      return { id, ...input };
    },
    deletePremiumReport: (_, { id }) => {
      // Placeholder: delete a premium report from the database and confirm the deletion
      return { id, Product_Name: "Deleted" };
    },
    addPremiumAdjustment: (_, { input }) => {
      // Placeholder: add a premium adjustment to the database and return it
      return { id: "1", ...input };
    },
    updatePremiumAdjustment: (_, { id, input }) => {
      // Placeholder: update a premium adjustment in the database and return it
      return { id, ...input };
    },
    deletePremiumAdjustment: (_, { id }) => {
      // Placeholder: delete a premium adjustment from the database and confirm the deletion
      return { id, Product_Name: "Deleted" };
    },
    addSinglePremiumCertificateReturn: (_, { input }) => {
      // Placeholder: add a single premium certificate return to the database and return it
      return { id: "1", ...input };
    },
    updateSinglePremiumCertificateReturn: (_, { id, input }) => {
      // Placeholder: update a single premium certificate return in the database and return it
      return { id, ...input };
    },
    deleteSinglePremiumCertificateReturn: (_, { id }) => {
      // Placeholder: delete a single premium certificate return from the database and confirm the deletion
      return { id };
    },
  },
};
resolver-codegen-end
```