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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292246"
---
# <a name="getpermissions-method-adox"></a><span data-ttu-id="e4672-102">Метод GetPermissions (ADOX)</span><span class="sxs-lookup"><span data-stu-id="e4672-102">GetPermissions method (ADOX)</span></span>

<span data-ttu-id="e4672-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e4672-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e4672-104">Возвращает разрешения для группы или пользователя в контейнере объекта или объекта.</span><span class="sxs-lookup"><span data-stu-id="e4672-104">Returns the permissions for a group or user on an object or object container.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4672-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4672-105">Syntax</span></span>

<span data-ttu-id="e4672-106">*ReturnValue*  =  *GroupOrUser*. GetPermissions(Имя , *ObjectType* , \[ *ObjectTypeId* \] )</span><span class="sxs-lookup"><span data-stu-id="e4672-106">*ReturnValue* = *GroupOrUser*.GetPermissions(*Name*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="e4672-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4672-107">Return value</span></span>

<span data-ttu-id="e4672-108">Возвращает значение **Long,** которое указывает битмаску, содержащую разрешения, которые группа или пользователь имеет на объекте.</span><span class="sxs-lookup"><span data-stu-id="e4672-108">Returns a **Long** value that specifies a bitmask containing the permissions that the group or user has on the object.</span></span> <span data-ttu-id="e4672-109">Это значение может быть одним или более из [констант RightsEnum.](rightsenum.md)</span><span class="sxs-lookup"><span data-stu-id="e4672-109">This value can be one or more of the [RightsEnum](rightsenum.md) constants.</span></span>

## <a name="parameters"></a><span data-ttu-id="e4672-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4672-110">Parameters</span></span>

|<span data-ttu-id="e4672-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="e4672-111">Parameter</span></span>|<span data-ttu-id="e4672-112">Описание</span><span class="sxs-lookup"><span data-stu-id="e4672-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="e4672-113">*Name*</span><span class="sxs-lookup"><span data-stu-id="e4672-113">*Name*</span></span> |<span data-ttu-id="e4672-114">Значение **Variant,** которое указывает имя объекта, для которого необходимо установить разрешения.</span><span class="sxs-lookup"><span data-stu-id="e4672-114">A **Variant** value that specifies the name of the object for which to set permissions.</span></span> <span data-ttu-id="e4672-115">Установите *значение* Имя null, если вы хотите получить разрешения для контейнера объекта.</span><span class="sxs-lookup"><span data-stu-id="e4672-115">Set *Name* to a null value if you want to get the permissions for the object container.</span></span>|
|<span data-ttu-id="e4672-116">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="e4672-116">*ObjectType*</span></span> |<span data-ttu-id="e4672-117">**Длинное** значение, которое может быть одной из констант [ObjectTypeEnum,](objecttypeenum.md) которое указывает тип объекта, для которого необходимо получить разрешения.</span><span class="sxs-lookup"><span data-stu-id="e4672-117">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="e4672-118">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="e4672-118">*ObjectTypeId*</span></span> |<span data-ttu-id="e4672-119">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="e4672-119">Optional.</span></span> <span data-ttu-id="e4672-120">Значение **Variant,** которое указывает GUID для типа объекта поставщика, не определенного спецификацией OLE DB.</span><span class="sxs-lookup"><span data-stu-id="e4672-120">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="e4672-121">Этот параметр необходим, если *objectType* задан **в adPermObjProviderSpecific;** в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="e4672-121">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

