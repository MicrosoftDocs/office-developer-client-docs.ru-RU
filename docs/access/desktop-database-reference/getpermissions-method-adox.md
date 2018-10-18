---
title: GetPermissions Method (ADOX)
TOCTitle: GetPermissions Method (ADOX)
ms:assetid: 98a2b2b6-a8af-15ee-b052-622a6f0661b9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249683(v=office.15)
ms:contentKeyID: 48546496
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 388cbc5a69f57778d8a9a46db8d1dbec5ddf09d6
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604967"
---
# <a name="getpermissions-method-adox"></a><span data-ttu-id="55cce-102">GetPermissions Method (ADOX)</span><span class="sxs-lookup"><span data-stu-id="55cce-102">GetPermissions Method (ADOX)</span></span>


<span data-ttu-id="55cce-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="55cce-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="55cce-104">Возвращает разрешения для группы или пользователя на объект или контейнер объектов.</span><span class="sxs-lookup"><span data-stu-id="55cce-104">Returns the permissions for a group or user on an object or object container.</span></span>

## <a name="syntax"></a><span data-ttu-id="55cce-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55cce-105">Syntax</span></span>

<span data-ttu-id="55cce-106">*ReturnValue* = *Группа_или_пользователь*. GetPermissions (*имя*, *тип объекта* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="55cce-106">*ReturnValue* = *GroupOrUser*.GetPermissions(*Name*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

<span data-ttu-id="55cce-107"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="55cce-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="55cce-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55cce-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="55cce-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55cce-109">Return value</span></span>
>>>>>>> <span data-ttu-id="55cce-110">master</span><span class="sxs-lookup"><span data-stu-id="55cce-110">master</span></span>

<span data-ttu-id="55cce-111">Возвращает значение типа **Long** , указывает битовую маску, содержащее разрешения для пользователей или групп в объекте.</span><span class="sxs-lookup"><span data-stu-id="55cce-111">Returns a **Long** value that specifies a bitmask containing the permissions that the group or user has on the object.</span></span> <span data-ttu-id="55cce-112">Это значение может быть один или несколько [RightsEnum](rightsenum.md) констант.</span><span class="sxs-lookup"><span data-stu-id="55cce-112">This value can be one or more of the [RightsEnum](rightsenum.md) constants.</span></span>

## <a name="parameters"></a><span data-ttu-id="55cce-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="55cce-113">Parameters</span></span>

  - <span data-ttu-id="55cce-114">*Имя*</span><span class="sxs-lookup"><span data-stu-id="55cce-114">*Name*</span></span>

  - <span data-ttu-id="55cce-115">Значение **типа Variant** , указывающее имя объекта, для которого необходимо задать разрешения.</span><span class="sxs-lookup"><span data-stu-id="55cce-115">A **Variant** value that specifies the name of the object for which to set permissions.</span></span> <span data-ttu-id="55cce-116">Задайте *имя* значение null, если вы хотите получить разрешения для объекта контейнера.</span><span class="sxs-lookup"><span data-stu-id="55cce-116">Set *Name* to a null value if you want to get the permissions for the object container.</span></span>

  - <span data-ttu-id="55cce-117">*Тип объекта*</span><span class="sxs-lookup"><span data-stu-id="55cce-117">*ObjectType*</span></span>

  - <span data-ttu-id="55cce-118">**Длинное целое** значение, который может быть одной из констант [ObjectTypeEnum](objecttypeenum.md) , которые указывает тип объекта, для которого необходимо получить разрешения.</span><span class="sxs-lookup"><span data-stu-id="55cce-118">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>

  - <span data-ttu-id="55cce-119">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="55cce-119">*ObjectTypeId*</span></span>

  - <span data-ttu-id="55cce-120">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="55cce-120">Optional.</span></span> <span data-ttu-id="55cce-121">Значение **типа Variant** , который указывает идентификатор GUID для поставщика тип объекта, не определена спецификацией OLE DB.</span><span class="sxs-lookup"><span data-stu-id="55cce-121">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="55cce-122">Этот параметр является обязательным, если *тип объекта* имеет значение **adPermObjProviderSpecific**; в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="55cce-122">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

