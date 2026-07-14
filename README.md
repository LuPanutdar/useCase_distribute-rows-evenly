# splitGrp — Split & Distribute Data into 3 Groups

An Excel Office Script that sorts data by a specified column and evenly distributes rows across three new worksheets in a round-robin fashion.

---

## What It Does

1. **Sorts** the data in the `Data` sheet by **column I** (descending order)
2. **Creates** three new worksheets automatically
3. **Copies the header row** to all three new sheets
4. **Distributes data rows evenly** across the three sheets using round-robin assignment:
   - Row 2 → Sheet 1
   - Row 3 → Sheet 2
   - Row 4 → Sheet 3
   - Row 5 → Sheet 1 *(repeats)*
   - ...and so on

---

## Requirements

- Microsoft 365 with Excel (desktop or web)
- A worksheet named **`Data`** in your workbook
- Data must have a **header row** in row 1
- **Column I** should contain the values you want to sort by (e.g., sales figures, scores, amounts)

---

## How to Use

1. Open your Excel workbook and make sure your data sheet is named **`Data`**
2. Go to the **Automate** tab in the Excel ribbon
3. Click **New Script**
4. Paste the contents of `splitGrp.ts` into the code editor
5. Click **Run**
6. Three new sheets will be created with your data evenly split

---

## Example

If your `Data` sheet has 10 data rows (rows 2–11), after running the script:

| Sheet | Rows assigned |
|-------|--------------|
| New Sheet 1 | Rows 2, 5, 8, 11 |
| New Sheet 2 | Rows 3, 6, 9 |
| New Sheet 3 | Rows 4, 7, 10 |

Each sheet will include the original header row.

---

## Notes

- The script adds new sheets each time it runs — rename or delete them between runs to avoid clutter
- The sort is applied **in place** on the `Data` sheet before splitting
- Column I is used as the sort key — update the script if your sort column is different

---

## Author

**Panutdar (Lu) Dremstedt**  
[LinkedIn](https://www.linkedin.com/in/panutdardremstedt-1b500b5b) · [GitHub](https://github.com/LuPanutdar/excel-office-scripts)
