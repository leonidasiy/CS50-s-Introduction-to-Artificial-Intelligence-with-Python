First Try:
    Conv2D(30, (3, 3), activation='relu', input_shape=(30, 30, 3)),
    MaxPooling2D(pool_size = (2, 2)),
    Flatten(),
    Dense(129, activation='sigmoid'),
    Dropout(0.5),
    Dense(NUM_CATEGORIES, activation='sigmoid')
    (11/11 - 0s - loss: 0.9162 - accuracy: 0.6399 - 68ms/epoch - 6ms/step)

Second Try:
    Conv2D(30, (3, 3), activation='relu', input_shape=(IMG_WIDTH, IMG_HEIGHT, 3)),
    MaxPooling2D(pool_size = (2, 2)),
    Flatten(),
    Dense(129, activation='relu'),
    Dropout(0.5),
    Dense(NUM_CATEGORIES, activation='softmax')
    (11/11 - 0s - loss: 0.0000e+00 - accuracy: 1.0000 - 70ms/epoch - 6ms/step)

Third Try:
    Conv2D(43, (3, 3), activation='relu', input_shape=(IMG_WIDTH, IMG_HEIGHT, 3)),
    MaxPooling2D(pool_size = (3, 3)),
    Flatten(),
    Dense(172, activation='relu'),
    Dropout(0.6),
    Dense(NUM_CATEGORIES, activation='softmax')
    (11/11 - 0s - loss: 0.0108 - accuracy: 0.9970 - 68ms/epoch - 6ms/step)