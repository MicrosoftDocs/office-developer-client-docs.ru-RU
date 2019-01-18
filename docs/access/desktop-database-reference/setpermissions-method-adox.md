---
title: Метод SetPermissions (ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f9b393e90d579c131865b112263efd0aef3216b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710288"
---
# <a name="setpermissions-method-adox"></a>Метод SetPermissions (ADOX)

**Применимо к**: Access 2013, Office 2013

Определяет разрешения для группы или пользователя на объект.

## <a name="syntax"></a>Синтаксис

*Группа_или_пользователь*. *Имя*, *тип объекта*, SetPermissions *Действие*, *правами* \[,*наследуют* \] \[,*ObjectTypeId*\]

## <a name="parameters"></a>Parameters

|Параметр|Описание|
|:--------|:----------|
|*Name* |**Строковое** значение, указывающее имя объекта, для которого необходимо задать разрешения.|
|*ObjectType* |**Длинное целое** значение, который может быть одной из констант [ObjectTypeEnum](objecttypeenum.md) , которые указывает тип объекта, для которого необходимо получить разрешения.|
|*Action* |**Длинное целое** значение, который может быть одной из констант [ActionEnum](actionenum.md) , указывает тип действие, выполняемое при установке разрешений.|
|*Права* |**Длинное целое** значение, который может быть битовой маски одного или нескольких константы [RightsEnum](rightsenum.md) , которые указывает прав для задания.|
|*Наследование* |Необязательно. **Длинное целое** значение, который может быть одной из констант [InheritTypeEnum](inherittypeenum.md) , определяющее, как наследование разрешений. Значение по умолчанию — **adInheritNone**.|
|*ObjectTypeId* |Необязательно. Значение **типа Variant** , который указывает идентификатор GUID для поставщика тип объекта, не определена спецификацией OLE DB. Этот параметр является обязательным, если *тип объекта* имеет значение **adPermObjProviderSpecific**; в противном случае он не используется.|

## <a name="remarks"></a>Замечания

Если поставщик поддерживает назначении прав доступа для групп или пользователей, произойдет ошибка.

> [!NOTE]
> При вызове **SetPermissions**Установка действия **adAccessRevoke** переопределяет все параметры параметр *правами* . Не установите для *действия* для **adAccessRevoke** правами, указанный в параметре *прав* вступили в силу.


