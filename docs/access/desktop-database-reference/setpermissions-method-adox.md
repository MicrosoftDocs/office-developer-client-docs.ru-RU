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
# <a name="setpermissions-method-adox"></a><span data-ttu-id="68d35-102">Метод SetPermissions (ADOX)</span><span class="sxs-lookup"><span data-stu-id="68d35-102">SetPermissions method (ADOX)</span></span>

<span data-ttu-id="68d35-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="68d35-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="68d35-104">Задает разрешения для группы или пользователя в объекте.</span><span class="sxs-lookup"><span data-stu-id="68d35-104">Specifies the permissions for a group or user on an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="68d35-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68d35-105">Syntax</span></span>

<span data-ttu-id="68d35-106">*Граупорусер*. SetPermissions*Name*, *ObjectType*, *Action*, *Rights* \[,*inherit* \] \[,*обжекттипеид*\]</span><span class="sxs-lookup"><span data-stu-id="68d35-106">*GroupOrUser*.SetPermissions*Name*, *ObjectType*, *Action*, *Rights* \[,*Inherit*\] \[,*ObjectTypeId*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="68d35-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="68d35-107">Parameters</span></span>

|<span data-ttu-id="68d35-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="68d35-108">Parameter</span></span>|<span data-ttu-id="68d35-109">Описание</span><span class="sxs-lookup"><span data-stu-id="68d35-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="68d35-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="68d35-110">*Name*</span></span> |<span data-ttu-id="68d35-111">**Строковое** значение, задающее имя объекта, для которого необходимо задать разрешения.</span><span class="sxs-lookup"><span data-stu-id="68d35-111">A **String** value that specifies the name of the object for which to set permissions.</span></span>|
|<span data-ttu-id="68d35-112">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="68d35-112">*ObjectType*</span></span> |<span data-ttu-id="68d35-113">**Длинное** значение, которое может быть одной из констант [обжекттипинум](objecttypeenum.md) , которое указывает тип объекта, для которого нужно получить разрешения.</span><span class="sxs-lookup"><span data-stu-id="68d35-113">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="68d35-114">*Действие*</span><span class="sxs-lookup"><span data-stu-id="68d35-114">*Action*</span></span> |<span data-ttu-id="68d35-115">**Длинное** значение, которое может быть одной из констант [актионенум](actionenum.md) , определяющих тип действия, выполняемого при задании разрешений.</span><span class="sxs-lookup"><span data-stu-id="68d35-115">A **Long** value which can be one of the [ActionEnum](actionenum.md) constants that specifies the type of action to perform when setting permissions.</span></span>|
|<span data-ttu-id="68d35-116">*Rights*</span><span class="sxs-lookup"><span data-stu-id="68d35-116">*Rights*</span></span> |<span data-ttu-id="68d35-117">**Длинное** значение, которое может быть битовой маской одной или нескольких констант [ригхтсенум](rightsenum.md) , указывающей права, которые необходимо задать.</span><span class="sxs-lookup"><span data-stu-id="68d35-117">A **Long** value which can be a bitmask of one or more of the [RightsEnum](rightsenum.md) constants, that indicates the rights to set.</span></span>|
|<span data-ttu-id="68d35-118">*Наследование*</span><span class="sxs-lookup"><span data-stu-id="68d35-118">*Inherit*</span></span> |<span data-ttu-id="68d35-119">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="68d35-119">Optional.</span></span> <span data-ttu-id="68d35-120">**Длинное** значение, которое может быть одной из констант [инхериттипинум](inherittypeenum.md) , которое указывает, как объекты будут наследовать эти разрешения.</span><span class="sxs-lookup"><span data-stu-id="68d35-120">A **Long** value which can be one of the [InheritTypeEnum](inherittypeenum.md) constants, that specifies how objects will inherit these permissions.</span></span> <span data-ttu-id="68d35-121">Значение по умолчанию — **адинхеритноне**.</span><span class="sxs-lookup"><span data-stu-id="68d35-121">The default value is **adInheritNone**.</span></span>|
|<span data-ttu-id="68d35-122">*обжекттипеид*</span><span class="sxs-lookup"><span data-stu-id="68d35-122">*ObjectTypeId*</span></span> |<span data-ttu-id="68d35-123">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="68d35-123">Optional.</span></span> <span data-ttu-id="68d35-124">Значение **Variant** , задающее GUID для типа объекта поставщика, не определенного СПЕЦИФИКАЦИЕЙ OLE DB.</span><span class="sxs-lookup"><span data-stu-id="68d35-124">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="68d35-125">Этот параметр является обязательным, если параметр *ObjectType* имеет значение **адпермобжпровидерспеЦифик**; в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="68d35-125">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="68d35-126">Примечания</span><span class="sxs-lookup"><span data-stu-id="68d35-126">Remarks</span></span>

<span data-ttu-id="68d35-127">Если поставщик не поддерживает установку прав доступа для групп или пользователей, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="68d35-127">An error will occur if the provider does not support setting access rights for groups or users.</span></span>

> [!NOTE]
> <span data-ttu-id="68d35-128">При вызове **SetPermissions**задание действий для **адакцессревоке** переопределяет все параметры параметра *Rights* .</span><span class="sxs-lookup"><span data-stu-id="68d35-128">When calling **SetPermissions**, setting Actions to **adAccessRevoke** overrides any settings of the *Rights* parameter.</span></span> <span data-ttu-id="68d35-129">Не задавайте *действия* в **адакцессревоке** , если необходимо, чтобы права, указанные в параметре *Rights* , вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="68d35-129">Do not set *Actions* to **adAccessRevoke** if you want the rights specified in the *Rights* parameter to take effect.</span></span>


