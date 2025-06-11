# Watermark Autoencoder

This project implements an autoencoder-based neural network designed to remove watermarks from images through reconstruction. It combines synthetic watermark generation, data augmentation, and stepwise training to achieve efficient learning in constrained environments.

## Project Overview

The goal is to train a neural network capable of reconstructing original (clean) images from inputs that contain watermarks. The project includes all key steps: from data preprocessing and augmentation to model training and evaluation.

## Task Objectives

### Stage 1

- Use clean images as input and programmatically apply watermarks (e.g., semi-transparent text overlay).
- Design an autoencoder architecture suitable for low-memory environments such as free-tier Google Colab.
- Train the model on watermarked images with the objective to reconstruct the clean version.
- Evaluate the model on a holdout test set.
- Visualize at least 10 test samples, including:
  - The original (clean) image
  - The watermarked image
  - The model’s reconstructed (predicted) image
  - The noise image (difference between prediction and ground truth)

### Stage 2 (Extended Task)

- Apply at least five distinct image augmentations (rotation, shift, noise, brightness change, etc.) to improve model robustness.
- Implement stepwise training over at least three stages:
  - Load and train on a subset of the data
  - Clear memory
  - Adjust training parameters (e.g., learning rate, batch size) for the next stage
  - Repeat until full dataset is covered

## Technologies Used

- Python 3
- TensorFlow / Keras
- OpenCV or PIL for image processing
- Albumentations for data augmentation
- Numpy, Matplotlib for preprocessing and visualization

## Results

The model successfully learned to reconstruct clean images from watermarked versions, preserving structural details and reducing visible watermark artifacts. Stepwise training helped optimize memory usage and generalization.

---

# Автокодировщик для удаления водяных знаков

Данный проект реализует нейросетевой автокодировщик для восстановления оригинальных изображений, искажённых водяными знаками. Используется генерация водяных знаков, аугментации и поэтапное обучение для эффективной работы в условиях ограниченной памяти.

## Описание проекта

Цель — обучить нейросеть восстанавливать чистые изображения по входным, содержащим водяные знаки. Проект охватывает полный цикл: от предобработки данных до визуализации результатов.

## Цели задания

### Этап 1

- Использовать чистые изображения и программно наносить на них водяные знаки (например, полупрозрачный текст).
- Разработать архитектуру автокодировщика, подходящую для ограниченной среды (например, Google Colab).
- Обучить модель на искажённых изображениях и научить её восстанавливать оригиналы.
- Оценить модель на тестовой выборке.
- Визуализировать не менее 10 примеров, включая:
  - Исходное (чистое) изображение  
  - Изображение с водяным знаком  
  - Восстановленное моделью изображение  
  - Шумовое изображение (разность между предсказанием и оригиналом)

### Этап 2 (расширенное задание)

- Применить минимум 5 различных аугментаций (поворот, сдвиг, шум, изменение яркости и т.д.).
- Реализовать поэтапное обучение (не менее 3 шагов):
  - Загрузить и обучить на части данных
  - Очистить память
  - При необходимости скорректировать параметры обучения
  - Повторить до охвата всего набора

## Используемые технологии

- Python 3
- TensorFlow / Keras
- OpenCV или PIL для работы с изображениями
- Albumentations для аугментаций
- Numpy, Matplotlib для визуализации и анализа

## Результаты

Модель успешно научилась восстанавливать изображения без водяных знаков, сохраняя структуру объектов и снижая искажения. Поэтапное обучение позволило эффективно использовать память и улучшить обобщающую способность.
