---
title: Метод GetPermissions (ADOX)
TOCTitle: GetPermissions method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 14cba54742a71a8b319f80b6fd1a910a85debcec
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926726"
---
# <a name="getpermissions-method-adox"></a>Метод GetPermissions (ADOX)


**Применимо к**: Access 2013, Office 2013


Возвращает разрешения для группы или пользователя на объект или контейнер объектов.

## <a name="syntax"></a>Синтаксис

*ReturnValue* = *Группа_или_пользователь*. GetPermissions (*имя*, *тип объекта* \[,*ObjectTypeId*\])

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение типа **Long** , указывает битовую маску, содержащее разрешения для пользователей или групп в объекте. Это значение может быть один или несколько [RightsEnum](rightsenum.md) констант.

## <a name="parameters"></a>Параметры

  - *Имя*

  - Значение **типа Variant** , указывающее имя объекта, для которого необходимо задать разрешения. Задайте *имя* значение null, если вы хотите получить разрешения для объекта контейнера.

  - *Тип объекта*

  - **Длинное целое** значение, который может быть одной из констант [ObjectTypeEnum](objecttypeenum.md) , которые указывает тип объекта, для которого необходимо получить разрешения.

  - *ObjectTypeId*

  - Необязательно указывать. Значение **типа Variant** , который указывает идентификатор GUID для поставщика тип объекта, не определена спецификацией OLE DB. Этот параметр является обязательным, если *тип объекта* имеет значение **adPermObjProviderSpecific**; в противном случае он не используется.

