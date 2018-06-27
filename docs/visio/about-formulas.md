---
title: Формулы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251823
localization_priority: Normal
ms.assetid: ec0de3e1-21dc-c5d6-2c2a-d5fef80d89bd
description: Ключ для управления действия фигуры является написание формул, которые определяют желаемое поведение. Вы можете изменить формулу ячейки изменять значение ячейки, и в результате изменить поведение конкретного фигуры. Например высота ячеек в разделе Преобразование фигуры содержит формулу, можно изменить для изменения фигуры высоту.
ms.openlocfilehash: 7df5ffe4d3dc32bcd5209bde353c39a92c7d422b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813105"
---
# <a name="about-formulas"></a>Формулы

Ключ для управления действия фигуры является написание формул, которые определяют желаемое поведение. Вы можете изменить формулу ячейки изменять значение ячейки, и в результате изменить поведение конкретного фигуры. Например высота ячеек в разделе Преобразование фигуры содержит формулу, можно изменить для изменения фигуры высоту.
  
Microsoft Visio формулы похожи на типичной электронной таблице формулы различными способами. Visio указаниям ничего в ячейке, даже если он является числовым значением или ссылка на ячейку простой, как формулы.
  
Формулы в ячейке можно наследуется от эквивалентный ячейка главный или стиля или определенные локально. Visio оцениваются формулы и затем преобразует результаты в соответствующее значение и соответствующие единицы измерения для ячейки. В окне таблицы свойств фигуры вы можете отобразить содержимое ячейки формулы или значения.
  
## <a name="elements-of-a-formula"></a>Элементы формулы

Формула всегда начинается с знак равенства, автоматически вставляется. Формула может содержать следующие элементы:
  
- �����
    
- Координаты
    
- Логические значения
    
- Операторы
    
- �������
    
- ������
    
- Ссылки на ячейки
    
- Единицы измерения
    
## <a name="default-formulas"></a>По умолчанию формул

При создании фигуры Visio создает формулы для него по умолчанию. Чтобы узнать, что формулы по умолчанию, нарисовать простую фигуру (прямоугольник, эллипс или прямой) и откройте его окно таблицы свойств фигуры (на вкладке [Разработчик](run-in-developer-mode-display-the-developer-tab.md) выберите **Показать таблицу свойств фигуры**).
  
## <a name="inherited-formulas"></a>Наследуемые формул

Visio наследует формул, когда это возможно. А не в экземпляре сделать локальной копии каждой формулы, экземпляр наследует формулы с его основного элементов документа и наследует параметры форматирования от определения стилей, хранятся вместе с документа. Это приводит к файлов меньшего размера, но также позволяет изменения главной формулы или определение стиля распространить все экземпляры.
  
Черный текст в ячейке указывает наследуемые формулы.
  
## <a name="local-formulas"></a>Локальные формулы

При записи локального формулу для экземпляра замены унаследованного формулы в ячейке локального переопределения. Будущие изменения в этой ячейке в основной или стиля не влияют на этот экземпляр, так как он был заблокирован наследования для ячейки с локального переопределения.
  
Применение стиля удаляет все локальные формулы в ячейках, связанных с ними, если не использовать функцию защиты для защиты.
  
Синий текст указывает локальную формулу, либо в результате редактирования формулы в окне таблицы свойств фигуры или некоторые изменения фигуры, в которой обнаружен Visio Сброс формулу для этой ячейки.
  
## <a name="automatic-updates-to-formulas"></a>Автоматические обновления для формул

 При любом изменении фигуры в документе Visio автоматически обновляет определенные ячейки. Это означает, что в некоторых случаях формул при вводе может быть заменен. Например при перетаскивании углового маркера для изменения размера фигуры Visio сбрасывает формулы в ячейках PinX, PinY, ширину и высоту. 
  
При необходимости можно защищать формулы от изменений с помощью функции защиты.
  
