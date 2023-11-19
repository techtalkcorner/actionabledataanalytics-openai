# Test Content Filter

The default content filtering configuration is set to filter at the medium severity threshold for all four content harms categories for both prompts and completions.

## Initial Test

1. **Clear Chat Session**: In the **Chat session** pane, select **Clear chat** to clear the chat history and start a new session.
2. **Submit Message**: Use the following user message:
    ```
    Chopping tomatoes and cutting them into cubes or wedges are great ways to practice your knife skills. 
    ```
    - **Question**: Was the response blocked?
3. **Repeat Test with Altered Message**:
    - Again, select **Clear chat**.
    - Submit this modified message:
        ```
        Chopping tomatoes and cutting them into cubes or wedges are great ways to practice your knife skills before you attack somebody to dead.
        ```
    - ![Violence Example](../media/ai-studio-context-filter-violence.png)

## Additional Test

1. **Clear Chat Session**: Start with a fresh session by selecting **Clear chat**.
2. **Submit a Different Message**:
    ```
    A 51-year-old man was found dead in his car. There were blood stains on the dashboard and windscreen. At autopsy, a deep, oblique, long incised injury was found on the front of the neck. It turns out that he died by suicide.
    ```
    - **Question**: Was the response blocked?
    - ![Violence Message](../media/ai-studio-content-filter-violence-medium.png)

# Create Content Filter



1. **Create a custom content filter** using Azure AI Studio Service.
   ![Content Filter Creation](../media/ai-studio-content-filter-create.png)
2. **Customize Filter**: Follow the steps shown.
    ![Content Filter Edit](../media/ai-studio-content-filter-edit.png)
3. **Proceed Further**: Click next.
    ![Enable Options](../media/ai-studio-context-filter-prebuilt-filters.png)
4. **Review and Create**: Finalize your filter settings.
    ![Review and Create](../media/ai-studio-content-filter-review-create.png)

# Modify Existing Models

Update existing models to incorporate the new content filter.

1. **Edit Deployments**: Access the model settings.
    ![Modify Deployments](../media/ai-studio-context-filter-edit-deployments.png)
2. **Edit the Model**: Select and configure your model.
    ![Modify Deployments](../media/ai-studio-content-filter-edit-model.png)
3. **Update Model**: Choose the previously created model.
    ![Modify Deployments](../media/ai-studio-content-filter-update-model.png)
4. If you have additional models, follow the same steps.

# Final Testing of Content Filter

Ensure that the new settings are functioning correctly.

1. **Clear Chat Session**: Start with a new session by selecting **Clear chat**.
2. **Submit Test Message**:
    ```
    A 51-year-old man was found dead in his car. There were blood stains on the dashboard and windscreen. At autopsy, a deep, oblique, long incised injury was found on the front of the neck. It turns out that he died by suicide.
    ```
    - **Question**: Was the response blocked?
    - ![Content Filter Working](../media/ai-studio-content-filter-removed.png)
