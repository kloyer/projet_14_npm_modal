# React Confirmation Modal

React Confirmation Modal is a reusable modal component for React applications. It provides a simple way to display confirmation dialogs with customizable content.

## Table of Contents

- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Getting Started

To get started with React Confirmation Modal, follow the instructions below.

### Prerequisites

Before you begin, make sure you have the following dependencies installed:

- React (^16.0.0)
- React DOM (^16.0.0)

### Installation

You can install React Confirmation Modal using npm or yarn.

npm install projet_14_npm_modal
or
yarn add projet_14_npm_modal

#### Usage

Once you've installed the package, you can use React Confirmation Modal in your React components.

import React, { useState } from 'react';
import ConfirmationModal from 'react-confirmation-modal';
import 'react-confirmation-modal/dist/ConfirmationModal.css';

const MyComponent = () => {
  const [isModalOpen, setIsModalOpen] = useState(false);

  const openModal = () => {
    setIsModalOpen(true);
  };

  const closeModal = () => {
    setIsModalOpen(false);
  };

  return (
    <div>
      <button onClick={openModal}>Open Confirmation Modal</button>
      <ConfirmationModal isOpen={isModalOpen} onClose={closeModal}>
        <h2>Confirmation</h2>
        <p>Are you sure you want to proceed?</p>
        <button onClick={closeModal}>Cancel</button>
        <button onClick={handleConfirm}>OK</button>
      </ConfirmationModal>
    </div>
  );
};

export default MyComponent;