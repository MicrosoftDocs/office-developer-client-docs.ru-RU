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

Предпочтительным методом программирования ADO с **\#** visual C++ является использование директивы импорта, как было рассмотрено в microsoft [Visual C++ ADO Programming.](visual-c-ado-programming.md) Однако более ранние версии ADO поставлялись с альтернативным методом программирования с использованием Visual C++: расширения Visual C++. В этом разделе документируется эта функция для тех, кто должен поддерживать код расширений Visual C++, но новый код ADO должен быть написан с помощью \# **импорта**.

Одно из самых утомительных заданий, с чем сталкиваются программисты Visual C++ при возвращении данных с помощью ADO, — преобразование данных, возвращаемого в виде типа данных VARIANT, в тип данных C++, а затем сохранение преобразованных данных в классе или структуре. Помимо того, что процесс является слишком утомительным, искомые данные C++ с помощью типа данных VARIANT снижают производительность.

ADO предоставляет интерфейс, который поддерживает искомые данные в нативных типах данных C/C++ без использования VARIANT, а также содержит макрос предварительной обработки, упрощающий использование интерфейса. Результатом является гибкое средство, которое проще в использовании и имеет большую производительность.

Распространенный сценарий клиента C/C++ — привязка записи в наборе [записей](recordset-object-ado.md) к структуре C/C++ или классу, содержащей нативные типы C/C++. При переходе через VARIANTs это включает написание кода преобразования из VARIANT в исходные типы C/C++. Расширения Visual C++ для ADO значительно упрощают этот сценарий для программиста Visual C++.

В следующих темах вы узнаете больше о расширениях Visual C++ для ADO.

  - [Использование расширений Visual C++ для ADO](using-visual-c-extensions.md)

  - [Visual C++ Extensions Header](visual-c-extensions-header.md)

  - [ADO with Visual C++ Extensions Example](visual-c-extensions-example.md)

