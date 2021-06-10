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

Указывает абсолютную строку URL-адреса, которая указывает на родительную [запись](record-object-ado.md) текущего объекта **Record.**

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **String,** которое указывает URL-адрес родительской **записи.**

## <a name="remarks"></a>Примечания

Свойство **ParentURL** зависит от источника, используемого для открытия **объекта Record.** Например, **запись может** быть открыта с источником, содержащим относительное имя пути каталога, ссылаясь на [свойство ActiveConnection.](activeconnection-property-ado.md)

Предположим, что "second" — это папка, содержаная под "первым". Откройте объект **Record** следующим образом:

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

Теперь значение свойства **ParentURL** — свойство **ParentURL** — ", то же самое, что https://first и **ActiveConnection.**

Источником также может быть абсолютный URL-адрес, например " https://first/second . Свойство **ParentURL** — это https://first ", уровень выше . Свойство **ParentURL** — это https://first ", уровень выше "second".

Это свойство может быть значением null, если:

- Для текущего объекта не существует родительского родителя; например, если **объект Record** представляет корень каталога.

- Объект **Record** представляет объект, который не может быть указан с URL-адресом.

Это свойство доступно только для чтения.


> [!NOTE]
> - Это свойство поддерживается только поставщиками источников документов, такими как [поставщик DB Microsoft OLE для публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md) Дополнительные сведения см. в [Provider-Supplied Records and Provider-Supplied Fields.](records-and-provider-supplied-fields.md)
> - URL-адреса, использующие схему http, автоматически вызывают поставщика DB Microsoft OLE для публикации в Интернете. Дополнительные сведения см. в [url-адресах Absolute и Relative.](absolute-and-relative-urls.md) 
> - Если текущая запись содержит запись данных из ADO **Recordset,** доступ к свойству **ParentURL** вызывает ошибку во время запуска, что указывает на невозможность URL-адреса.


