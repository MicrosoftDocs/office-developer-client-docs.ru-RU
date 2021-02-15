---
title: Программирование ADO/WFC
TOCTitle: ADO/WFC programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 904b5e3930c0e7e7b1d98f94bd39cfbf816aa145
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283207"
---
# <a name="adowfc-programming"></a>Программирование ADO/WFC

**Область применения**: Access 2013, Office 2013

Для Microsoft Visual J++ 6.0 ADO был расширен для работы с классами Windows Foundation (WFC) следующими способами. Во-первых, реализован набор классов Java, который расширяет интерфейсы ADO и создает уведомления, интересные программисту java; Классы Java также предоставляет функции, возвращая пользователю типы Java. Чтобы повысить производительность, класс Java напрямую имеет доступ к нативным типам данных в объекте OLE DB rowset и возвращает их программисту Java в качестве типов Java, не преобразуя их в вариант и из него. ADO также был расширен для работы с уведомлениями о событиях в структуре WFC.

ADO для классов Windows Foundation (ADO/WFC) поддерживает все стандартные методы ADO, свойства, объекты и события. Однако операции, которые требуют варианта в качестве параметра и показывают отличную производительность на таких языках, как Microsoft Visual Basic, отображают меньшую производительность на таких языках, как Visual J++. По этой причине ADO/WFC также предоставляет дополнительные функции для объекта [Field,](field-object-ado.md) которые принимают машинные типы данных Java вместо типа данных variant.

Дополнительные сведения в документации ADO о пакетах ADO/WFC см. в описании синтаксиса [ADO/WFC.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/ado-wfc-syntax-index)

## <a name="referencing-the-library"></a>Ссылка на библиотеку

Чтобы импортировать классы данных ADO/WFC в проект, включите в свой код следующую строку:

```java 
 
import com.ms.wfc.data.*; 
```

