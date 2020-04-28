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

Указывает строку абсолютного URL-адреса, указывающую на родительскую [запись](record-object-ado.md) текущего объекта **Record** .

## <a name="return-value"></a>Возвращаемое значение

Возвращает **строковое** значение, указывающее URL-адрес родительской **записи**.

## <a name="remarks"></a>Примечания

Свойство **ParentURL** зависит от источника, используемого для открытия объекта **Record** . Например, **запись** может быть открыта с источником, содержащим относительный путь к каталогу, на который ссылается свойство [ActiveConnection](activeconnection-property-ado.md) .

Предположим, что "Second" — это папка, которая находится в разделе "First". Откройте объект **Record** , выполнив следующие действия:

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

Теперь значение свойства **ParentURL** равно **ParentURL** свойству "https://first", то же, что и **ActiveConnection**.

Источник также может быть абсолютным URL-адресом, напримерhttps://first/second, "". В качестве значения свойства **ParentURL** используетсяhttps://firstуровень выше. В качестве значения свойства **ParentURL** используетсяhttps://firstуровень выше "второй".

Это свойство может иметь значение null, если:

- Родительский объект для текущего объекта отсутствует; Например, если объект **Record** представляет корень каталога.

- Объект **Record** представляет сущность, которая не может быть указана с URL-адресом.

Это свойство доступно только для чтения.


> [!NOTE]
> - Это свойство поддерживается только поставщиками источника документов, такими как [поставщик Microsoft OLE DB для публикации в Интернете](microsoft-ole-db-provider-for-internet-publishing.md). Для получения дополнительных сведений см [записи и поля, предоставляемые поставщиком](records-and-provider-supplied-fields.md).
> - URL-адреса, использующие схему HTTP, автоматически будут вызывать поставщик Microsoft OLE DB для публикации в Интернете. Для получения дополнительных сведений см [абсолютные и относительные URL-адреса](absolute-and-relative-urls.md). 
> - Если текущая запись содержит запись данных из **набора записей**ADO, то при доступе к свойству **ParentURL** возникает ошибка времени выполнения, указывающая на то, что URL-адрес невозможен.


