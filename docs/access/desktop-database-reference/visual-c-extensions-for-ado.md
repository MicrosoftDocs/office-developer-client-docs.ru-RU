---
title: Расширения Visual C++ для ADO
TOCTitle: Visual C++ Extensions for ADO
ms:assetid: 38048ae0-1dae-9e5e-c569-04011df8b5aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249134(v=office.15)
ms:contentKeyID: 48544212
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fc69d3244cf6faf3aa91fe954e4b39323cf13abf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302756"
---
# <a name="visual-c-extensions-for-ado"></a>Расширения Visual C++ для ADO


**Область применения**: Access 2013, Office 2013

Предпочтительным методом программирования ADO с **\#** Visual C++ является использование директивы импорта, как это Microsoft Visual C++ [ADO Programming.](visual-c-ado-programming.md) Однако более ранние версии ADO поставляются с альтернативным методом программирования с помощью Visual C++: Visual C++ Extensions. В этом разделе документируется эта функция для тех, кто должен поддерживать код расширений Visual C++, но новый код ADO должен быть написан с помощью \# **импорта.**

Одна из самых утомительных задач, с чем сталкиваются программисты Visual C++ при сборе данных с помощью ADO, — преобразование данных, возвращающихся в виде типа данных VARIANT, в тип данных C++, а затем хранение преобразованных данных в классе или структуре. В дополнение к тому, что они являются громоздкими, сбор данных C++ с помощью типа данных VARIANT снижает производительность.

ADO предоставляет интерфейс, который поддерживает сбор данных в родные типы данных C/C++ без использования VARIANT, а также макрос предпроцессора, упрощающий использование интерфейса. В результате это гибкий инструмент, который проще в использовании и имеет большую производительность.

Распространенный клиентский сценарий C/C++ — привязка записи в [Наборе](recordset-object-ado.md) записей к структуре C/C++ или классу, содержащим родные типы C/C++. При переходе на VARIANTs это включает написание кода преобразования из VARIANT в типы C/C++ . Расширение Visual C++ для ADO нацелено на то, чтобы значительно упростить этот сценарий для программиста Visual C++.

Дополнительные разделы о расширении Visual C++ для ADO см. в следующих разделах.

  - [Использование расширений Visual C++ для ADO](using-visual-c-extensions.md)

  - [Visual C++ Extensions Header](visual-c-extensions-header.md)

  - [Пример ADO с визуальными расширениями C++](visual-c-extensions-example.md)

