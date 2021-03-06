---
title: Свойство EditMode (ADO)
TOCTitle: EditMode property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d7bba0af804df89bf4c8611e184928c9bf12d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293611"
---
# <a name="editmode-property-ado"></a>Свойство EditMode (ADO)


**Область применения**: Access 2013, Office 2013

Указывает состояние редактирования текущей записи.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение [EditModeEnum.](editmodeenum.md)

## <a name="remarks"></a>Примечания

ADO поддерживает буфер редактирования, связанный с текущей записью. Это свойство указывает, были ли внесены изменения в этот буфер или создана новая запись. Чтобы определить состояние редактирования текущей записи, используйте свойство **EditMode.** Вы можете проверить ожидающие изменения, если процесс редактирования был прерван, и определить, нужно ли использовать метод [Update](update-method-ado.md) или [CancelUpdate.](cancelupdate-method-ado.md)

Дополнительные сведения о свойстве **EditMode** в различных условиях редактирования см. в методе [AddNew.](addnew-method-ado.md)

Если вызов [](delete-method-ado-recordset.md) удалить не удалит запись или записи в источнике данных (например, из-за нарушений целостности ссылок), [recordset](recordset-object-ado.md) будет оставаться в режиме редактирования **(EditMode**  =  **adEditInProgress).** Это означает, что перед отключением текущей записи [(например,](move-method-ado.md)Move, [NextRecordset](nextrecordset-method-ado.md)или [Close)](close-method-ado.md)необходимо созвали **CancelUpdate.**


> [!NOTE]
> **EditMode** может вернуть допустимые значения только при текущей записи. **EditMode** возвращает ошибку, если boF или [EOF](bof-eof-properties-ado.md) верны, или если текущая запись удалена.


