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

Возвращает владельца объекта в [каталоге](catalog-object-adox.md).

## <a name="syntax"></a>Синтаксис

*Owner* = *Каталог*владельца. GetObjectOwner (*имя_объекта*, *ObjectType* \[,*обжекттипеид*\])

## <a name="return-value"></a>Возвращаемое значение

Возвращает **строковое** значение, задающее [имя](name-property-adox.md) [пользователя](user-object-adox.md) или [группы](group-object-adox.md) , которые являются владельцами объекта.

## <a name="parameters"></a>Параметры

|Параметр|Описание|
|:--------|:----------|
|*ObjectName* |**Строковое** значение, задающее имя объекта, для которого требуется возвратить владельца.|
|*ObjectType* |**Длинное** значение, которое может быть одной из констант [обжекттипинум](objecttypeenum.md) , которое указывает тип объекта, для которого требуется получить владельца.|
|*обжекттипеид* |Необязательное. Значение **Variant** , задающее GUID для типа объекта поставщика, не определенного СПЕЦИФИКАЦИЕЙ OLE DB. Этот параметр является обязательным, если параметр *ObjectType* имеет значение **адпермобжпровидерспеЦифик**; в противном случае он не используется.|

## <a name="remarks"></a>Примечания

Если поставщик не поддерживает возврат владельцев объекта, произойдет ошибка.

