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

Для Microsoft Visual J++ 6.0 ADO была расширена для работы с Windows классами фонда (WFC) следующими способами. Во-первых, реализован набор классов Java, который расширяет интерфейсы ADO и создает уведомления, интересные программисту Java; Классы Java также раскрывают функции, возвращая типы Java пользователю. Чтобы повысить производительность, класс Java напрямую имеет доступ к родным типам данных в объекте rowset OLE DB и возвращает их программисту Java в качестве типов Java, не преобразовав их в вариант и из него. ADO также расширена для работы с уведомлениями о событиях в рамках WFC.

ADO для Windows классов Foundation (ADO/WFC) поддерживает все стандартные методы ADO, свойства, объекты и события. Однако операции, которые требуют варианта в качестве параметра и демонстрируют отличную производительность на таком языке, как Microsoft Visual Basic, отображают меньшую производительность на языке, например Visual J++. По этой причине ADO/WFC также предоставляет вспомогательные функции на [объекте Field,](field-object-ado.md) который принимает родные типы данных Java, а не тип данных вариантов.

Дополнительные сведения в документации ADO о пакетах ADO/WFC см. в индексе [синтаксиса ADO/WFC.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/ado-wfc-syntax-index)

## <a name="referencing-the-library"></a>Ссылки на библиотеку

Чтобы импортировать классы данных ADO/WFC в проект, включите в код следующую строку:

```java 
 
import com.ms.wfc.data.*; 
```

