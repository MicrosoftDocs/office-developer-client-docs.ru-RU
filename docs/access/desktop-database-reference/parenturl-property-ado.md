---
title: ParentURL Property (ADO)
TOCTitle: ParentURL Property (ADO)
ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15)
ms:contentKeyID: 48548517
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0fb5e8683bcf7ebe0905b21f169f71834ed424e4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483160"
---
# <a name="parenturl-property-ado"></a>ParentURL Property (ADO)

**Применимо к**: Access 2013 | Office 2013

Указывает строку абсолютный URL-адрес, указывающий на родительской [записи](record-object-ado.md) текущего объекта **записи** .

## <a name="return-value"></a>Возвращаемое значение

Возвращает **строковое** значение, которое указывает URL-адрес родительской **записи**.

## <a name="remarks"></a>Замечания

Свойство **ParentURL** зависит от источника, используемого для открытия объект **записи** . Например, **записи** можно открыть с источником, содержащий относительный путь каталог, указанный в свойстве [ActiveConnection](activeconnection-property-ado.md) .

Предположим, что «second» папки содержится в разделе «первый». Откройте объект **записи** со следующими:

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

Сейчас, — это значение свойства **ParentURL** **ParentURL** свойством является "https://first", то же, что **ActiveConnection**.

Источник также могут быть абсолютный URL-адрес например, "https://first/second". Является ли данное свойство **ParentURL** нажмите "https://first", уровень выше. Является ли данное свойство **ParentURL** нажмите "https://first", уровень выше «секунды».

Это свойство может иметь значение null, если:

- Родительского объекта нет текущего объекта; Например, если объект **записи** представляет корневой каталог.

- Объект **записи** представляет сущности, которая не может быть указан URL-адрес.

Это свойство доступно только для чтения.


> [!NOTE]
> - Это свойство поддерживается только с поставщиками исходного документа, такими как [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md). Для получения дополнительных сведений см [записей и Provider-Supplied полей](records-and-provider-supplied-fields.md).
> - URL-адреса, с помощью схемы http автоматически вызывает поставщик Microsoft OLE DB для публикации Интернет. Для получения дополнительных сведений см [абсолютного и относительных URL-адресов](absolute-and-relative-urls.md). 
> - Если текущая запись содержит записи данных из набора **записей**ADO, доступ к свойству **ParentURL** вызывает ошибку времени выполнения, указывающего на то, что URL-адрес не является возможных.


