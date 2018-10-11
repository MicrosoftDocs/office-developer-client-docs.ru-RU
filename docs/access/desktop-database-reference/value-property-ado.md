---
title: Value Property (ADO)
TOCTitle: Value Property (ADO)
ms:assetid: ff21d122-98e3-2b48-d92f-e696b8079fc5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250310(v=office.15)
ms:contentKeyID: 48548958
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 68c0d45345dfc768f5d435689abf67bcc3d9abe2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480006"
---
# <a name="value-property-ado"></a>Value Property (ADO)


**Применимо к**: Access 2013 | Office 2013

Указывает значение, присваиваемое [поля](field-object-ado.md), [параметр](parameter-object-ado.md)или [Свойства](property-object-ado.md) объекта.

## <a name="settings-and-return-values"></a>Параметры и возвращаемые значения

Задает или возвращает значение **типа Variant** , которое указывает значение объекта. Значение по умолчанию зависит от [типа](type-property-ado.md) свойства.

## <a name="remarks"></a>Замечания

Используйте свойство **Value** задает или возвращает данные из **поля** объектов, изменять или возвращаемые значения параметра с объектами **параметров** для или установить параметры свойств с помощью **Свойства** объектов. Является ли **значение** свойства чтения и записи или только для чтения зависит от множество факторов, обратитесь к соответствующим разделам соответствующего объекта для получения дополнительных сведений.

ADO позволяет установку и возврат двоичные данные с помощью свойства **Value** .


> [!NOTE]
> <P>Для <STRONG>параметра</STRONG> объекты ADO считывает свойство <STRONG>Value</STRONG> только один раз от поставщика. Если команда содержит <STRONG>параметр</STRONG> , свойство <STRONG>Value</STRONG> является пустым и создание <A href="recordset-object-ado.md">набора записей</A> с помощью команды, убедитесь, что после закрытия <STRONG>набора записей</STRONG> перед загрузкой свойство <STRONG>Value</STRONG> . В противном случае для некоторых поставщиков свойство <STRONG>Value</STRONG> может быть пустым и не содержит правильное значение.</P>



Для нового **поля** объектов, к коллекции [полей](fields-collection-ado.md) объекта [записи](record-object-ado.md) свойство **Value** необходимо установить перед можно указать любые другие свойства **поля** . Во-первых определенного значения для свойства **Value** должна быть назначена и вызове [Update](update-method-ado.md) в коллекции **полей** . Затем осуществляется другие свойства, такие как [Тип](type-property-ado.md) или [атрибуты](attributes-property-ado.md) .

