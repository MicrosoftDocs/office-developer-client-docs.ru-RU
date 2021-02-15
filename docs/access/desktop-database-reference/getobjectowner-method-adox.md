---
title: Метод GetObjectOwner (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 948464534f9bbfbea50c8eba2c926dea9cb9bcac
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292260"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="28206-102">Метод GetObjectOwner (ADOX)</span><span class="sxs-lookup"><span data-stu-id="28206-102">GetObjectOwner method (ADOX)</span></span>

<span data-ttu-id="28206-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="28206-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="28206-104">Возвращает владельца объекта в [каталоге.](catalog-object-adox.md)</span><span class="sxs-lookup"><span data-stu-id="28206-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="28206-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28206-105">Syntax</span></span>

<span data-ttu-id="28206-106">*Владелец*  =  *Каталог .* GetObjectOwner(*ObjectName*, *ObjectType* \[ ,*ObjectTypeId* \] )</span><span class="sxs-lookup"><span data-stu-id="28206-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="28206-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="28206-107">Return value</span></span>

<span data-ttu-id="28206-108">Возвращает **строку,** которая указывает имя [](user-object-adox.md) пользователя [](group-object-adox.md) или группы, владельцем объекта. [](name-property-adox.md)</span><span class="sxs-lookup"><span data-stu-id="28206-108">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="28206-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="28206-109">Parameters</span></span>

|<span data-ttu-id="28206-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="28206-110">Parameter</span></span>|<span data-ttu-id="28206-111">Описание</span><span class="sxs-lookup"><span data-stu-id="28206-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="28206-112">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="28206-112">*ObjectName*</span></span> |<span data-ttu-id="28206-113">**Строковая** строка, которая указывает имя объекта, для которого возвращается владелец.</span><span class="sxs-lookup"><span data-stu-id="28206-113">A **String** value that specifies the name of the object for which to return the owner.</span></span>|
|<span data-ttu-id="28206-114">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="28206-114">*ObjectType*</span></span> |<span data-ttu-id="28206-115">Длинное значение, которое может быть одной из [констант ObjectTypeEnum,](objecttypeenum.md) которое указывает тип объекта, для которого необходимо получить владельца. </span><span class="sxs-lookup"><span data-stu-id="28206-115">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>|
|<span data-ttu-id="28206-116">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="28206-116">*ObjectTypeId*</span></span> |<span data-ttu-id="28206-117">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="28206-117">Optional.</span></span> <span data-ttu-id="28206-118">Значение **Variant,** которое указывает GUID для типа объекта поставщика, не определенного спецификацией OLE DB.</span><span class="sxs-lookup"><span data-stu-id="28206-118">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="28206-119">Этот параметр обязален, если *для ObjectType* задан параметр **adPermObjProviderSpecific;** в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="28206-119">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="28206-120">Заметки</span><span class="sxs-lookup"><span data-stu-id="28206-120">Remarks</span></span>

<span data-ttu-id="28206-121">Если поставщик не поддерживает возвращение владельцев объектов, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="28206-121">An error will occur if the provider does not support returning object owners.</span></span>

