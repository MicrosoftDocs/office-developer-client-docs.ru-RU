---
title: Метод GetObjectOwner (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 948464534f9bbfbea50c8eba2c926dea9cb9bcac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292260"
---
# <a name="getobjectowner-method-adox"></a>Метод GetObjectOwner (ADOX)

**Область применения**: Access 2013, Office 2013

Возвращает владельца объекта в [каталоге.](catalog-object-adox.md)

## <a name="syntax"></a>Синтаксис

*Владелец*  =  *Каталог .* GetObjectOwner(*ObjectName*, *ObjectType* \[ ,*ObjectTypeId* \] )

## <a name="return-value"></a>Возвращаемое значение

Возвращает **строку,** которая указывает имя [](user-object-adox.md) пользователя [](group-object-adox.md) или группы, владельцем объекта. [](name-property-adox.md)

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*ObjectName* |**Строковая** строка, которая указывает имя объекта, для которого возвращается владелец.|
|*ObjectType* |Длинное значение, которое может быть одной из [констант ObjectTypeEnum,](objecttypeenum.md) которое указывает тип объекта, для которого необходимо получить владельца. |
|*ObjectTypeId* |Необязательный параметр. Значение **Variant,** которое указывает GUID для типа объекта поставщика, не определенного спецификацией OLE DB. Этот параметр обязален, если *для ObjectType* задан параметр **adPermObjProviderSpecific;** в противном случае он не используется.|

## <a name="remarks"></a>Заметки

Если поставщик не поддерживает возвращение владельцев объектов, произойдет ошибка.

