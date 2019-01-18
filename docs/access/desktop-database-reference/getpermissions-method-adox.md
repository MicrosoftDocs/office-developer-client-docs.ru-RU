---
title: Метод GetPermissions (ADOX)
TOCTitle: GetPermissions method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa5dda3c8e2ee8251fc54f4ff3bc12be0aca5002
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719745"
---
# <a name="getpermissions-method-adox"></a><span data-ttu-id="f183c-102">Метод GetPermissions (ADOX)</span><span class="sxs-lookup"><span data-stu-id="f183c-102">GetPermissions method (ADOX)</span></span>

<span data-ttu-id="f183c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f183c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f183c-104">Возвращает разрешения для группы или пользователя на объект или контейнер объектов.</span><span class="sxs-lookup"><span data-stu-id="f183c-104">Returns the permissions for a group or user on an object or object container.</span></span>

## <a name="syntax"></a><span data-ttu-id="f183c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f183c-105">Syntax</span></span>

<span data-ttu-id="f183c-106">*ReturnValue* = *Группа_или_пользователь*. GetPermissions (*имя*, *тип объекта* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="f183c-106">*ReturnValue* = *GroupOrUser*.GetPermissions(*Name*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="f183c-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f183c-107">Return value</span></span>

<span data-ttu-id="f183c-108">Возвращает значение типа **Long** , указывает битовую маску, содержащее разрешения для пользователей или групп в объекте.</span><span class="sxs-lookup"><span data-stu-id="f183c-108">Returns a **Long** value that specifies a bitmask containing the permissions that the group or user has on the object.</span></span> <span data-ttu-id="f183c-109">Это значение может быть один или несколько [RightsEnum](rightsenum.md) констант.</span><span class="sxs-lookup"><span data-stu-id="f183c-109">This value can be one or more of the [RightsEnum](rightsenum.md) constants.</span></span>

## <a name="parameters"></a><span data-ttu-id="f183c-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="f183c-110">Parameters</span></span>

|<span data-ttu-id="f183c-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="f183c-111">Parameter</span></span>|<span data-ttu-id="f183c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f183c-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="f183c-113">*Name*</span><span class="sxs-lookup"><span data-stu-id="f183c-113">*Name*</span></span> |<span data-ttu-id="f183c-114">Значение **типа Variant** , указывающее имя объекта, для которого необходимо задать разрешения.</span><span class="sxs-lookup"><span data-stu-id="f183c-114">A **Variant** value that specifies the name of the object for which to set permissions.</span></span> <span data-ttu-id="f183c-115">Задайте *имя* значение null, если вы хотите получить разрешения для объекта контейнера.</span><span class="sxs-lookup"><span data-stu-id="f183c-115">Set *Name* to a null value if you want to get the permissions for the object container.</span></span>|
|<span data-ttu-id="f183c-116">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="f183c-116">*ObjectType*</span></span> |<span data-ttu-id="f183c-117">**Длинное целое** значение, который может быть одной из констант [ObjectTypeEnum](objecttypeenum.md) , которые указывает тип объекта, для которого необходимо получить разрешения.</span><span class="sxs-lookup"><span data-stu-id="f183c-117">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="f183c-118">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="f183c-118">*ObjectTypeId*</span></span> |<span data-ttu-id="f183c-119">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="f183c-119">Optional.</span></span> <span data-ttu-id="f183c-120">Значение **типа Variant** , который указывает идентификатор GUID для поставщика тип объекта, не определена спецификацией OLE DB.</span><span class="sxs-lookup"><span data-stu-id="f183c-120">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="f183c-121">Этот параметр является обязательным, если *тип объекта* имеет значение **adPermObjProviderSpecific**; в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="f183c-121">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

