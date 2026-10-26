# Test Cases: Vidya Saathi

These are manual test cases derived from the current code in `index.html`. **Execution status is Not run** until a person performs the steps in a browser. The expected outcomes describe the current implementation, including its limitations.

| ID | Scenario | Steps / input | Expected result | Status |
|---|---|---|---|---|
| TC-01 | Initial load | Open `index.html` | Welcome message, subject buttons, and teacher dashboard appear | Not run |
| TC-02 | Select Math | Click Math | Math question about `1/2 + 1/3` appears | Not run |
| TC-03 | Accepted Math answer | Select Math; enter `5/6` | Correct feedback appears | Not run |
| TC-04 | Recognized Math misconception | Select Math; enter `2/5` | Feedback about adding numerators and denominators appears; “Common denominators (Class 5)” count increases on first attempt | Not run |
| TC-05 | Math hint | Select Math; enter an unrecognized wrong answer | First predefined hint appears | Not run |
| TC-06 | Science accepted answer | Select Science; enter an answer containing `conduct` | Correct feedback appears because matching is substring-based | Not run |
| TC-07 | Recognized Science misconception | Select Science; enter `steam` | Targeted heat-transfer feedback appears and the relevant count is updated on first attempt | Not run |
| TC-08 | Social Studies accepted answer | Select Social; enter `Godavari` | Correct feedback appears | Not run |
| TC-09 | Recognized Social Studies misconception | Select Social; enter `Ganga` | Targeted feedback about peninsular and Himalayan rivers appears | Not run |
| TC-10 | Blank input | Submit an empty or whitespace-only answer | No new chat message is added for the blank input | Not run |
| TC-11 | Enter key | Type an answer and press Enter | The answer is submitted, same as clicking Send | Not run |
| TC-12 | Unrecognized answers beyond hints | Select a subject and repeatedly enter unrelated wrong answers until hints are exhausted | A worked explanation appears and the active question is cleared | Not run |
| TC-13 | Reload persistence | Trigger a concept-gap increment, then reload the page | Session increments reset; the dashboard returns to hard-coded sample counts | Not run |
| TC-14 | Sample CSV relationship | Open `data/sample_student_learning_data.csv` | Fictional records are visible; the current app does not import them | Not run |

## Notes

- The application does not include an automated test runner.
- Answer matching is simple and may accept or reject phrasing unexpectedly.
- A count update is triggered only by a recognized misconception pattern and only once per question attempt sequence, according to the current logic.
- Record actual outcomes and date if these tests are executed; do not change status to Passed without testing.
