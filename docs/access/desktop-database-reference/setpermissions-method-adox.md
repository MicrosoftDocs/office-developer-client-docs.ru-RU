---
title: SetPermissions Method (ADOX)
TOCTitle: SetPermissions Method (ADOX)
ms:assetid: 63d1053d-fb32-456b-ae67-3a4e45aa01af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249382(v=office.15)
ms:contentKeyID: 48545274
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 35578de28509e510e9ba5329cfdabc2eff8207b1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482249"
---
# <a name="setpermissions-method-adox"></a><span data-ttu-id="3cd04-102">SetPermissions Method (ADOX)</span><span class="sxs-lookup"><span data-stu-id="3cd04-102">SetPermissions Method (ADOX)</span></span>


<span data-ttu-id="3cd04-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3cd04-103">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="3cd04-104">Определяет разрешения для группы или пользователя на объект.</span><span class="sxs-lookup"><span data-stu-id="3cd04-104">Specifies the permissions for a group or user on an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cd04-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3cd04-105">Syntax</span></span>

<span data-ttu-id="3cd04-106">*Группа_или_пользователь*. *Имя*, *тип объекта*, SetPermissions *Действие*, *правами* \[,*наследуют* \] \[,*ObjectTypeId*\]</span><span class="sxs-lookup"><span data-stu-id="3cd04-106">*GroupOrUser*.SetPermissions*Name*, *ObjectType*, *Action*, *Rights* \[,*Inherit*\] \[,*ObjectTypeId*\]</span></span>

## <a name="parameters"></a><span data-ttu-id="3cd04-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3cd04-107">Parameters</span></span>

  - <span data-ttu-id="3cd04-108">*Имя*</span><span class="sxs-lookup"><span data-stu-id="3cd04-108">*Name*</span></span>

  - <span data-ttu-id="3cd04-109">**Строковое** значение, указывающее имя объекта, для которого необходимо задать разрешения.</span><span class="sxs-lookup"><span data-stu-id="3cd04-109">A **String** value that specifies the name of the object for which to set permissions.</span></span>

  - <span data-ttu-id="3cd04-110">*Тип объекта*</span><span class="sxs-lookup"><span data-stu-id="3cd04-110">*ObjectType*</span></span>

  - <span data-ttu-id="3cd04-111">**Длинное целое** значение, который может быть одной из констант [ObjectTypeEnum](objecttypeenum.md) , которые указывает тип объекта, для которого необходимо получить разрешения.</span><span class="sxs-lookup"><span data-stu-id="3cd04-111">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>

  - <span data-ttu-id="3cd04-112">*Действие*</span><span class="sxs-lookup"><span data-stu-id="3cd04-112">*Action*</span></span>

  - <span data-ttu-id="3cd04-113">**Длинное целое** значение, который может быть одной из констант [ActionEnum](actionenum.md) , указывает тип действие, выполняемое при установке разрешений.</span><span class="sxs-lookup"><span data-stu-id="3cd04-113">A **Long** value which can be one of the [ActionEnum](actionenum.md) constants that specifies the type of action to perform when setting permissions.</span></span>

  - <span data-ttu-id="3cd04-114">*Права*</span><span class="sxs-lookup"><span data-stu-id="3cd04-114">*Rights*</span></span>

  - <span data-ttu-id="3cd04-115">**Длинное целое** значение, который может быть битовой маски одного или нескольких константы [RightsEnum](rightsenum.md) , которые указывает прав для задания.</span><span class="sxs-lookup"><span data-stu-id="3cd04-115">A **Long** value which can be a bitmask of one or more of the [RightsEnum](rightsenum.md) constants, that indicates the rights to set.</span></span>

  - <span data-ttu-id="3cd04-116">*Наследование*</span><span class="sxs-lookup"><span data-stu-id="3cd04-116">*Inherit*</span></span>

  - <span data-ttu-id="3cd04-117">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="3cd04-117">Optional.</span></span> <span data-ttu-id="3cd04-118">**Длинное целое** значение, который может быть одной из констант [InheritTypeEnum](inherittypeenum.md) , определяющее, как наследование разрешений.</span><span class="sxs-lookup"><span data-stu-id="3cd04-118">A **Long** value which can be one of the [InheritTypeEnum](inherittypeenum.md) constants, that specifies how objects will inherit these permissions.</span></span> <span data-ttu-id="3cd04-119">Значение по умолчанию — **adInheritNone**.</span><span class="sxs-lookup"><span data-stu-id="3cd04-119">The default value is **adInheritNone**.</span></span>

  - <span data-ttu-id="3cd04-120">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="3cd04-120">*ObjectTypeId*</span></span>

  - <span data-ttu-id="3cd04-121">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="3cd04-121">Optional.</span></span> <span data-ttu-id="3cd04-122">Значение **типа Variant** , который указывает идентификатор GUID для поставщика тип объекта, не определена спецификацией OLE DB.</span><span class="sxs-lookup"><span data-stu-id="3cd04-122">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="3cd04-123">Этот параметр является обязательным, если *тип объекта* имеет значение **adPermObjProviderSpecific**; в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="3cd04-123">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cd04-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="3cd04-124">Remarks</span></span>

<span data-ttu-id="3cd04-125">Если поставщик поддерживает назначении прав доступа для групп или пользователей, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="3cd04-125">An error will occur if the provider does not support setting access rights for groups or users.</span></span>


> [!NOTE]
> <P><span data-ttu-id="3cd04-126">При вызове <STRONG>SetPermissions</STRONG>Установка действия <STRONG>adAccessRevoke</STRONG> переопределяет все параметры параметр <EM>правами</EM> .</span><span class="sxs-lookup"><span data-stu-id="3cd04-126">When calling <STRONG>SetPermissions</STRONG>, setting Actions to <STRONG>adAccessRevoke</STRONG> overrides any settings of the <EM>Rights</EM> parameter.</span></span> <span data-ttu-id="3cd04-127">Не установите для <EM>действия</EM> для <STRONG>adAccessRevoke</STRONG> правами, указанный в параметре <EM>прав</EM> вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="3cd04-127">Do not set <EM>Actions</EM> to <STRONG>adAccessRevoke</STRONG> if you want the rights specified in the <EM>Rights</EM> parameter to take effect.</span></span></P>


