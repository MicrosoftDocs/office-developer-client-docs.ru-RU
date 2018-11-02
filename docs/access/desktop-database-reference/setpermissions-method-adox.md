---
title: Метод SetPermissions (ADOX)
TOCTitle: SetPermissions method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d99608a938598135d713375875da9073c8f9f3c
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927517"
---
# <a name="setpermissions-method-adox"></a>Метод SetPermissions (ADOX)


**Применимо к**: Access 2013, Office 2013



Определяет разрешения для группы или пользователя на объект.

## <a name="syntax"></a>Синтаксис

*Группа_или_пользователь*. *Имя*, *тип объекта*, SetPermissions *Действие*, *правами* \[,*наследуют* \] \[,*ObjectTypeId*\]

## <a name="parameters"></a>Параметры

  - *Имя*

  - **Строковое** значение, указывающее имя объекта, для которого необходимо задать разрешения.

  - *Тип объекта*

  - **Длинное целое** значение, который может быть одной из констант [ObjectTypeEnum](objecttypeenum.md) , которые указывает тип объекта, для которого необходимо получить разрешения.

  - *Действие*

  - **Длинное целое** значение, который может быть одной из констант [ActionEnum](actionenum.md) , указывает тип действие, выполняемое при установке разрешений.

  - *Права*

  - **Длинное целое** значение, который может быть битовой маски одного или нескольких константы [RightsEnum](rightsenum.md) , которые указывает прав для задания.

  - *Наследование*

  - Необязательно указывать. **Длинное целое** значение, который может быть одной из констант [InheritTypeEnum](inherittypeenum.md) , определяющее, как наследование разрешений. Значение по умолчанию — **adInheritNone**.

  - *ObjectTypeId*

  - Необязательно указывать. Значение **типа Variant** , который указывает идентификатор GUID для поставщика тип объекта, не определена спецификацией OLE DB. Этот параметр является обязательным, если *тип объекта* имеет значение **adPermObjProviderSpecific**; в противном случае он не используется.

## <a name="remarks"></a>Примечания

Если поставщик поддерживает назначении прав доступа для групп или пользователей, произойдет ошибка.


> [!NOTE]
> <P>При вызове <STRONG>SetPermissions</STRONG>Установка действия <STRONG>adAccessRevoke</STRONG> переопределяет все параметры параметр <EM>правами</EM> . Не установите для <EM>действия</EM> для <STRONG>adAccessRevoke</STRONG> правами, указанный в параметре <EM>прав</EM> вступили в силу.</P>


