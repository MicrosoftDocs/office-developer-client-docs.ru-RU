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

Для Microsoft Visual J++ 6,0 объекты ADO были расширены для работы с классами Windows Foundation (WFC) следующими способами. В первую очередь реализован набор классов Java, расширяющий интерфейсы ADO и создающий уведомления, представляющие интерес для программиста Java; классы Java также предоставляют функции, возвращающие для пользователя типы Java. Для повышения производительности класс Java напрямую получает доступ к собственным типам данных в объекте набора строк OLE DB и возвращает их программистам Java как типы Java без предварительного преобразования их в тип Variant и обратно. Кроме того, ADO был расширен для работы с уведомлениями о событиях в платформе WFC Framework.

Классы ADO для Windows Foundation (ADO/WFC) поддерживают все стандартные методы, свойства, объекты и события ADO. Тем не менее, операции, требующие использования Variant в качестве параметра и показывающие отличное быстродействие на языке, например Microsoft Visual Basic, отображают меньшую производительность на таком языке, как Visual J++. По этой причине ADO/WFC также предоставляет функции для доступа к объекту [field](field-object-ado.md) , которые используют собственные типы данных Java вместо типа данных Variant.

Более подробную информацию о пакетах ADO/WFC можно узнать в статье [индекс синтаксиса ADO/WFC](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/ado-wfc-syntax-index).

## <a name="referencing-the-library"></a>Создание ссылок на библиотеку

Чтобы импортировать классы данных ADO/WFC в свой проект, добавьте в код следующую строку:

```java 
 
import com.ms.wfc.data.*; 
```

