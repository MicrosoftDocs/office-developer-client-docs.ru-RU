---
title: Свойство ParentURL (ADO)
TOCTitle: ParentURL property (ADO)
ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15)
ms:contentKeyID: 48548517
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8e3735147f813d904c206910ff319913f056946e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287719"
---
# <a name="parenturl-property-ado"></a>Свойство ParentURL (ADO)

**Область применения**: Access 2013, Office 2013

Указывает абсолютную строку URL-адреса, которая указывает на родительская [запись](record-object-ado.md) текущего объекта **Record.**

## <a name="return-value"></a>Возвращаемое значение

Возвращает **строку,** которая указывает URL-адрес родительской **записи.**

## <a name="remarks"></a>Заметки

Свойство **ParentURL** зависит от источника, используемого для открытия **объекта Record.** Например, запись **может** быть открыта с источником, содержащим относительный путь к каталогу, на который ссылается свойство [ActiveConnection.](activeconnection-property-ado.md)

Предположим, что "second" — это папка, вложенная в папку "first". Откройте объект **Record** со следующими объектами:

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

Теперь свойство **ParentURL** имеет значение **ParentURL** ", то же самое, что https://first и **ActiveConnection.**

Источником также может быть абсолютный URL-адрес, например " https://first/second . The **ParentURL** property is then https://first " , the level above . The **ParentURL** property is then https://first " , the level above "second" .

Это свойство может иметь значение NULL, если:

- Для текущего объекта не существует родительского объекта; например, если **объект Record** представляет корневой каталог.

- Объект **Record** представляет сущность, которую нельзя у указывает с помощью URL-адреса.

Это свойство доступно только для чтения.


> [!NOTE]
> - Это свойство поддерживается только поставщиками источников документов, такими как [поставщик Microsoft OLE DB для публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md) Дополнительные сведения [см. в записях и Provider-Supplied полях.](records-and-provider-supplied-fields.md)
> - URL-адреса, использующие схему HTTP, автоматически вызывают поставщика Microsoft OLE DB для интернет-публикации. Дополнительные сведения см. в сведениях [об абсолютных и относительных URL-адресах.](absolute-and-relative-urls.md) 
> - Если текущая запись содержит запись данных из объекта ADO **Recordset,** доступ к свойству **ParentURL** приводит к ошибке во время запуска, указывающей на то, что URL-адрес невозможен.


