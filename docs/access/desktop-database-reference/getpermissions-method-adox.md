---
title: Метод-Permissions (ADOX)
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
# <a name="getpermissions-method-adox"></a><span data-ttu-id="b59c1-102">Метод-Permissions (ADOX)</span><span class="sxs-lookup"><span data-stu-id="b59c1-102">GetPermissions method (ADOX)</span></span>

<span data-ttu-id="b59c1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b59c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b59c1-104">Возвращает разрешения для группы или пользователя в контейнере объекта или объекта.</span><span class="sxs-lookup"><span data-stu-id="b59c1-104">Returns the permissions for a group or user on an object or object container.</span></span>

## <a name="syntax"></a><span data-ttu-id="b59c1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b59c1-105">Syntax</span></span>

<span data-ttu-id="b59c1-106">*ReturnValue* = *граупорусер*. При наличии полномочий (*Name*, *ObjectType* \[,*обжекттипеид*\])</span><span class="sxs-lookup"><span data-stu-id="b59c1-106">*ReturnValue* = *GroupOrUser*.GetPermissions(*Name*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="b59c1-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b59c1-107">Return value</span></span>

<span data-ttu-id="b59c1-108">Возвращает значение **типа Long** , задающее битовую маску, содержащую разрешения, которые группа или пользователь имеет для объекта.</span><span class="sxs-lookup"><span data-stu-id="b59c1-108">Returns a **Long** value that specifies a bitmask containing the permissions that the group or user has on the object.</span></span> <span data-ttu-id="b59c1-109">Это значение может быть одной или несколькими константами [ригхтсенум](rightsenum.md) .</span><span class="sxs-lookup"><span data-stu-id="b59c1-109">This value can be one or more of the [RightsEnum](rightsenum.md) constants.</span></span>

## <a name="parameters"></a><span data-ttu-id="b59c1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b59c1-110">Parameters</span></span>

|<span data-ttu-id="b59c1-111">Параметр</span><span class="sxs-lookup"><span data-stu-id="b59c1-111">Parameter</span></span>|<span data-ttu-id="b59c1-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b59c1-112">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b59c1-113">*Name*</span><span class="sxs-lookup"><span data-stu-id="b59c1-113">*Name*</span></span> |<span data-ttu-id="b59c1-114">Значение **Variant** , задающее имя объекта, для которого необходимо задать разрешения.</span><span class="sxs-lookup"><span data-stu-id="b59c1-114">A **Variant** value that specifies the name of the object for which to set permissions.</span></span> <span data-ttu-id="b59c1-115">Задайте для свойства *Name* значение null, если вы хотите получить разрешения для контейнера объектов.</span><span class="sxs-lookup"><span data-stu-id="b59c1-115">Set *Name* to a null value if you want to get the permissions for the object container.</span></span>|
|<span data-ttu-id="b59c1-116">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="b59c1-116">*ObjectType*</span></span> |<span data-ttu-id="b59c1-117">**Длинное** значение, которое может быть одной из констант [обжекттипинум](objecttypeenum.md) , которое указывает тип объекта, для которого нужно получить разрешения.</span><span class="sxs-lookup"><span data-stu-id="b59c1-117">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get permissions.</span></span>|
|<span data-ttu-id="b59c1-118">*Обжекттипеид*</span><span class="sxs-lookup"><span data-stu-id="b59c1-118">*ObjectTypeId*</span></span> |<span data-ttu-id="b59c1-119">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="b59c1-119">Optional.</span></span> <span data-ttu-id="b59c1-120">Значение **Variant** , задающее GUID для типа объекта поставщика, не определенного СПЕЦИФИКАЦИЕЙ OLE DB.</span><span class="sxs-lookup"><span data-stu-id="b59c1-120">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="b59c1-121">Этот параметр является обязательным, если параметр *ObjectType* имеет значение **адпермобжпровидерспеЦифик**; в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="b59c1-121">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

