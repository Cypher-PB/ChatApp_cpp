# Qt Chat Application

## Overview

The Qt Chat Application is a simple, multi-conversation chat interface built using the Qt framework. It allows users to initiate new conversations, send and receive messages, and maintain multiple conversation windows simultaneously. This project serves as an example of managing GUI components, user input, and dynamic content updates in a Qt-based application.

## Features

- **Multi-Conversation Management**: Start and manage multiple conversations with different contacts.
- **Dynamic Conversation Windows**: Each conversation is displayed in its own window with a scrollable area for messages and an input field for sending new messages.
- **User-Friendly Interface**: Easy-to-use dialog for starting new conversations and clear separation of conversation windows.
- **Extensible Architecture**: The project is structured to be easily extended with new features such as message history, network communication, and more.

## Components

### MainWindow

The `MainWindow` class serves as the central hub of the application, managing the list of conversations and the creation of new conversation windows.

#### Key Attributes:
- `QListView* conversationListView`: Displays the list of current conversations.
- `QStringListModel* conversationModel`: Model to manage the list data for `conversationListView`.
- `QStringList conversations`: Stores the names of all conversations.
- `QMap<QString, QWidget*> conversationWindows`: Maps conversation names to their respective window widgets.

#### Key Methods:
- `void startNewConversation()`: Prompts the user to enter a friend's name and starts a new conversation.
- `void sendMessage()`: Sends a message in the current conversation window.

### Conversation Window Components

Each conversation window consists of:
- `QScrollArea`: A scrollable area that contains a `QLabel` to display messages.
- `QLabel`: Displays the messages in the conversation.
- `QTextEdit`: Input field for composing new messages.
- `QPushButton`: Button to send the composed message.

## Getting Started

### Prerequisites

- **Qt Framework**: Ensure you have the Qt framework installed. You can download it from [Qt's official website](https://www.qt.io/download).

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/qt-chat-application.git
   cd qt-chat-application
