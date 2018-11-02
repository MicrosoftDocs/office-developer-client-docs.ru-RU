---
title: Метод GetObjectOwner (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1a37b0f341c849358b649c2222df2955fd88f5d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927819"
---
# <a name="getobjectowner-method-adox"></a>Метод GetObjectOwner (ADOX)


**Применимо к**: Access 2013, Office 2013


Возвращает владельца объекта в [каталоге](catalog-object-adox.md).

## <a name="syntax"></a>Синтаксис

*Владелец* = *каталога*. GetObjectOwner (*имя объекта*, *ObjectType* \[,*ObjectTypeId*\])

## <a name="return-value"></a>Возвращаемое значение

Возвращает **строковое** значение, задающее [имя](name-property-adox.md) [пользователя](user-object-adox.md) или [группы](group-object-adox.md) , которому принадлежит объект.

## <a name="parameters"></a>Параметры

  - *Имя объекта*

  - **Строковое** значение, указывающее имя объекта, для которого возвращаются владельца.

  - *Тип объекта*

  - **Длинное целое** значение, который может быть одной из констант [ObjectTypeEnum](objecttypeenum.md) , указывает тип объекта, для которого необходимо получить владельца.

  - *ObjectTypeId*

  - Необязательно указывать. Значение **типа Variant** , который указывает идентификатор GUID для поставщика тип объекта, не определена спецификацией OLE DB. Этот параметр является обязательным, если *тип объекта* имеет значение **adPermObjProviderSpecific**; в противном случае он не используется.

## <a name="remarks"></a>Примечания

Если поставщик поддерживает возвращает ошибку владельцы объектов, произойдет ошибка.

