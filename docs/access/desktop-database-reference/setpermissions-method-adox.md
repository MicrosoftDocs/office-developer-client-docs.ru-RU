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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314583"
---
# <a name="setpermissions-method-adox"></a><span data-ttu-id="23659-102">Метод SetPermissions (ADOX)</span><span class="sxs-lookup"><span data-stu-id="23659-102">SetPermissions method (ADOX)</span></span>

<span data-ttu-id="23659-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="23659-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="23659-104">Указывает разрешения для группы или пользователя объекта.</span><span class="sxs-lookup"><span data-stu-id="23659-104">Specifies the permissions for a group or user on an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="23659-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23659-105">Syntax</span></span>

<span data-ttu-id="23659-106">*GroupOrUser*. SetPermissions *Name,* *ObjectType*, *Action*, *Rights* \[ ,*Inherit* \] \[ ,*ObjectTypeId*\]</span><span class="sxs-lookup"><span data-stu-id="23659-106">*GroupOrUser*.SetPermissions *Name*, *ObjectType*, *Action*, *Rights* \[,*Inherit*\] \[,*ObjectTypeId*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="23659-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="23659-107">Parameters</span></span>

|<span data-ttu-id="23659-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="23659-108">Parameter</span></span>|<span data-ttu-id="23659-109">Описание</span><span class="sxs-lookup"><span data-stu-id="23659-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="23659-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="23659-110">*Name*</span></span> |<span data-ttu-id="23659-111">Значение **String,** которое указывает имя объекта, для которого необходимо установить разрешения.</span><span class="sxs-lookup"><span data-stu-id="23659-111">A **String** value that specifies the name of the object for which to set permissions.</span></span>|
|<span data-ttu-id="23659-112">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="23659-112">*ObjectType*</span></span> |<span data-ttu-id="23659-113">**Длинное** значение, которое может быть одной из констант [ObjectTypeEnum,](objecttypeenum.md) которое указывает тип объекта, для которого необходимо получить разрешения.</span><span class="sxs-lookup"><span data-stu-id="23659-113">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="23659-114">*Действие*</span><span class="sxs-lookup"><span data-stu-id="23659-114">*Action*</span></span> |<span data-ttu-id="23659-115">**Длинное** значение, которое может быть одним из констант [ActionEnum,](actionenum.md) которое указывает тип действий, выполняемых при установке разрешений.</span><span class="sxs-lookup"><span data-stu-id="23659-115">A **Long** value which can be one of the [ActionEnum](actionenum.md) constants that specifies the type of action to perform when setting permissions.</span></span>|
|<span data-ttu-id="23659-116">*Rights*</span><span class="sxs-lookup"><span data-stu-id="23659-116">*Rights*</span></span> |<span data-ttu-id="23659-117">**Длинное** значение, которое может быть битом одной или более констант [RightsEnum,](rightsenum.md) которое указывает права на набор.</span><span class="sxs-lookup"><span data-stu-id="23659-117">A **Long** value which can be a bitmask of one or more of the [RightsEnum](rightsenum.md) constants, that indicates the rights to set.</span></span>|
|<span data-ttu-id="23659-118">*Наследование*</span><span class="sxs-lookup"><span data-stu-id="23659-118">*Inherit*</span></span> |<span data-ttu-id="23659-119">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="23659-119">Optional.</span></span> <span data-ttu-id="23659-120">**Длинное** значение, которое может быть одним из [констант InheritTypeEnum,](inherittypeenum.md) которое указывает, как объекты будут наследовать эти разрешения.</span><span class="sxs-lookup"><span data-stu-id="23659-120">A **Long** value which can be one of the [InheritTypeEnum](inherittypeenum.md) constants, that specifies how objects will inherit these permissions.</span></span> <span data-ttu-id="23659-121">По умолчанию значение **adInheritNone**.</span><span class="sxs-lookup"><span data-stu-id="23659-121">The default value is **adInheritNone**.</span></span>|
|<span data-ttu-id="23659-122">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="23659-122">*ObjectTypeId*</span></span> |<span data-ttu-id="23659-123">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="23659-123">Optional.</span></span> <span data-ttu-id="23659-124">Значение **Variant,** которое указывает GUID для типа объекта поставщика, не определенного спецификацией OLE DB.</span><span class="sxs-lookup"><span data-stu-id="23659-124">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="23659-125">Этот параметр необходим, если *objectType* задан **в adPermObjProviderSpecific;** в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="23659-125">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="23659-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="23659-126">Remarks</span></span>

<span data-ttu-id="23659-127">Ошибка произойдет, если поставщик не поддерживает установку прав доступа для групп или пользователей.</span><span class="sxs-lookup"><span data-stu-id="23659-127">An error will occur if the provider does not support setting access rights for groups or users.</span></span>

> [!NOTE]
> <span data-ttu-id="23659-128">При **вызове SetPermissions** настройка **Действия для adAccessRevoke** переопределяет все параметры *параметра Rights.*</span><span class="sxs-lookup"><span data-stu-id="23659-128">When calling **SetPermissions**, setting Actions to **adAccessRevoke** overrides any settings of the *Rights* parameter.</span></span> <span data-ttu-id="23659-129">Не *задайте действия* **adAccessRevoke,** если вы хотите, чтобы права, указанные в параметре *Rights,* вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="23659-129">Do not set *Actions* to **adAccessRevoke** if you want the rights specified in the *Rights* parameter to take effect.</span></span>


