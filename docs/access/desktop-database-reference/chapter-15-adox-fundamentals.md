---
title: Глава 15. Основы ADOX
TOCTitle: 'Chapter 15: ADOX fundamentals'
ms:assetid: 973d7579-4f34-3b31-a761-a951ab29e850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249673(v=office.15)
ms:contentKeyID: 48546464
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0e46920ba47dba018944768ff61c970781e37a02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296453"
---
# <a name="chapter-15-adox-fundamentals"></a>Глава 15. Основы ADOX

**Область применения**: Access 2013, Office 2013

Расширения объектов данных Microsoft ActiveX для языка описания данных и безопасности (ADOX) — это расширение для объектов и модели программирования ADO. ADOX включают объекты для создания и изменения схемы, а также для системы безопасности. Так как это основанный на объектах способ управления схемой, можно написать код, который будет работать с разными источниками данных, независимо от различий в их собственных синтаксисах.

ADOX — это дополнительная библиотека для основных объектов ADO. В ней представлены дополнительные объекты для создания, изменения и удаления объектов схемы, таких как таблицы и процедуры. В ней также содержатся объекты безопасности для обслуживания пользователей и групп, а также предоставления и отзыва разрешений для объектов.

Чтобы использовать ADOX с помощью средства разработки, необходимо установить ссылку на библиотеку типов ADOX. Описание библиотеки ADOX — "Microsoft ADO Ext. для DDL и security". Имя файла библиотеки ADOX Msadox.dll, а программный ID (ProgID) — ADOX. Дополнительные сведения о создании ссылок на библиотеки см. в документации средства разработки.

Поставщик microsoft OLE DB для microsoft Jet ядро СУБД полностью поддерживает ADOX. Некоторые функции ADOX могут не поддерживаться в зависимости от поставщика данных. Дополнительные сведения о поддерживаемых функциях с поставщиком microsoft OLE DB для ODBC, поставщик OLE DB для Oracle (Майкрософт) или Microsoft SQL Server OLE DB Provider см. в файле readme MDAC.

В этом документе предполагается знание языка программирования microsoft Visual Basic и общее знание ADO. Дополнительные сведения об ADO см. в руководстве [программиста ADO.](ado-programmer-s-guide.md)

В этой главе описывается следующая тема:

- [Поддержка поставщиков для ADOX](provider-support-for-adox.md)

Дополнительные сведения об ADOX см. в следующих разделах:

- [Объекты ADOX](adox-objects.md)
- [Коллекции ADOX](adox-collections.md)
- [Свойства ADOX](adox-properties.md)
- [Методы ADOX](adox-methods.md)
- [Примеры ADOX](adox-code-examples.md)

