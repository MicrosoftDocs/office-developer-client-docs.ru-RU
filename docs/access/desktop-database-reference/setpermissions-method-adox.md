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
# <a name="setpermissions-method-adox"></a><span data-ttu-id="abde1-102">Метод SetPermissions (ADOX)</span><span class="sxs-lookup"><span data-stu-id="abde1-102">SetPermissions method (ADOX)</span></span>

<span data-ttu-id="abde1-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="abde1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="abde1-104">Определяет разрешения для группы или пользователя на объект.</span><span class="sxs-lookup"><span data-stu-id="abde1-104">Specifies the permissions for a group or user on an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="abde1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abde1-105">Syntax</span></span>

<span data-ttu-id="abde1-106">*Группа_или_пользователь*. *Имя*, *тип объекта*, SetPermissions *Действие*, *правами* \[,*наследуют* \] \[,*ObjectTypeId*\]</span><span class="sxs-lookup"><span data-stu-id="abde1-106">*GroupOrUser*.SetPermissions*Name*, *ObjectType*, *Action*, *Rights* \[,*Inherit*\] \[,*ObjectTypeId*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="abde1-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="abde1-107">Parameters</span></span>

|<span data-ttu-id="abde1-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="abde1-108">Parameter</span></span>|<span data-ttu-id="abde1-109">Описание</span><span class="sxs-lookup"><span data-stu-id="abde1-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="abde1-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="abde1-110">*Name*</span></span> |<span data-ttu-id="abde1-111">**Строковое** значение, указывающее имя объекта, для которого необходимо задать разрешения.</span><span class="sxs-lookup"><span data-stu-id="abde1-111">A **String** value that specifies the name of the object for which to set permissions.</span></span>|
|<span data-ttu-id="abde1-112">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="abde1-112">*ObjectType*</span></span> |<span data-ttu-id="abde1-113">**Длинное целое** значение, который может быть одной из констант [ObjectTypeEnum](objecttypeenum.md) , которые указывает тип объекта, для которого необходимо получить разрешения.</span><span class="sxs-lookup"><span data-stu-id="abde1-113">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="abde1-114">*Action*</span><span class="sxs-lookup"><span data-stu-id="abde1-114">*Action*</span></span> |<span data-ttu-id="abde1-115">**Длинное целое** значение, который может быть одной из констант [ActionEnum](actionenum.md) , указывает тип действие, выполняемое при установке разрешений.</span><span class="sxs-lookup"><span data-stu-id="abde1-115">A **Long** value which can be one of the [ActionEnum](actionenum.md) constants that specifies the type of action to perform when setting permissions.</span></span>|
|<span data-ttu-id="abde1-116">*Права*</span><span class="sxs-lookup"><span data-stu-id="abde1-116">*Rights*</span></span> |<span data-ttu-id="abde1-117">**Длинное целое** значение, который может быть битовой маски одного или нескольких константы [RightsEnum](rightsenum.md) , которые указывает прав для задания.</span><span class="sxs-lookup"><span data-stu-id="abde1-117">A **Long** value which can be a bitmask of one or more of the [RightsEnum](rightsenum.md) constants, that indicates the rights to set.</span></span>|
|<span data-ttu-id="abde1-118">*Наследование*</span><span class="sxs-lookup"><span data-stu-id="abde1-118">*Inherit*</span></span> |<span data-ttu-id="abde1-119">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="abde1-119">Optional.</span></span> <span data-ttu-id="abde1-120">**Длинное целое** значение, который может быть одной из констант [InheritTypeEnum](inherittypeenum.md) , определяющее, как наследование разрешений.</span><span class="sxs-lookup"><span data-stu-id="abde1-120">A **Long** value which can be one of the [InheritTypeEnum](inherittypeenum.md) constants, that specifies how objects will inherit these permissions.</span></span> <span data-ttu-id="abde1-121">Значение по умолчанию — **adInheritNone**.</span><span class="sxs-lookup"><span data-stu-id="abde1-121">The default value is **adInheritNone**.</span></span>|
|<span data-ttu-id="abde1-122">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="abde1-122">*ObjectTypeId*</span></span> |<span data-ttu-id="abde1-123">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="abde1-123">Optional.</span></span> <span data-ttu-id="abde1-124">Значение **типа Variant** , который указывает идентификатор GUID для поставщика тип объекта, не определена спецификацией OLE DB.</span><span class="sxs-lookup"><span data-stu-id="abde1-124">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="abde1-125">Этот параметр является обязательным, если *тип объекта* имеет значение **adPermObjProviderSpecific**; в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="abde1-125">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="abde1-126">Замечания</span><span class="sxs-lookup"><span data-stu-id="abde1-126">Remarks</span></span>

<span data-ttu-id="abde1-127">Если поставщик поддерживает назначении прав доступа для групп или пользователей, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="abde1-127">An error will occur if the provider does not support setting access rights for groups or users.</span></span>

> [!NOTE]
> <span data-ttu-id="abde1-128">При вызове **SetPermissions**Установка действия **adAccessRevoke** переопределяет все параметры параметр *правами* .</span><span class="sxs-lookup"><span data-stu-id="abde1-128">When calling **SetPermissions**, setting Actions to **adAccessRevoke** overrides any settings of the *Rights* parameter.</span></span> <span data-ttu-id="abde1-129">Не установите для *действия* для **adAccessRevoke** правами, указанный в параметре *прав* вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="abde1-129">Do not set *Actions* to **adAccessRevoke** if you want the rights specified in the *Rights* parameter to take effect.</span></span>


