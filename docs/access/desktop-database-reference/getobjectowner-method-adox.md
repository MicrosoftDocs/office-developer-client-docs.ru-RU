---
title: Метод GetObjectOwner (ADOX)
TOCTitle: GetObjectOwner Method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6961cb1de192e480ca68d9688105600ac85c69c9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874218"
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

  - Необязательный параметр. Значение **типа Variant** , который указывает идентификатор GUID для поставщика тип объекта, не определена спецификацией OLE DB. Этот параметр является обязательным, если *тип объекта* имеет значение **adPermObjProviderSpecific**; в противном случае он не используется.

## <a name="remarks"></a>Замечания

Если поставщик поддерживает возвращает ошибку владельцы объектов, произойдет ошибка.

