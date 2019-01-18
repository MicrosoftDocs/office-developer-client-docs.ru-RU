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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710734"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="d1de8-102">Метод GetObjectOwner (ADOX)</span><span class="sxs-lookup"><span data-stu-id="d1de8-102">GetObjectOwner method (ADOX)</span></span>

<span data-ttu-id="d1de8-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d1de8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d1de8-104">Возвращает владельца объекта в [каталоге](catalog-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="d1de8-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1de8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1de8-105">Syntax</span></span>

<span data-ttu-id="d1de8-106">*Владелец* = *каталога*. GetObjectOwner (*имя объекта*, *ObjectType* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="d1de8-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="d1de8-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1de8-107">Return value</span></span>

<span data-ttu-id="d1de8-108">Возвращает **строковое** значение, задающее [имя](name-property-adox.md) [пользователя](user-object-adox.md) или [группы](group-object-adox.md) , которому принадлежит объект.</span><span class="sxs-lookup"><span data-stu-id="d1de8-108">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1de8-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="d1de8-109">Parameters</span></span>

|<span data-ttu-id="d1de8-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="d1de8-110">Parameter</span></span>|<span data-ttu-id="d1de8-111">Описание</span><span class="sxs-lookup"><span data-stu-id="d1de8-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d1de8-112">*Имя объекта*</span><span class="sxs-lookup"><span data-stu-id="d1de8-112">*ObjectName*</span></span> |<span data-ttu-id="d1de8-113">**Строковое** значение, указывающее имя объекта, для которого возвращаются владельца.</span><span class="sxs-lookup"><span data-stu-id="d1de8-113">A **String** value that specifies the name of the object for which to return the owner.</span></span>|
|<span data-ttu-id="d1de8-114">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="d1de8-114">*ObjectType*</span></span> |<span data-ttu-id="d1de8-115">**Длинное целое** значение, который может быть одной из констант [ObjectTypeEnum](objecttypeenum.md) , указывает тип объекта, для которого необходимо получить владельца.</span><span class="sxs-lookup"><span data-stu-id="d1de8-115">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>|
|<span data-ttu-id="d1de8-116">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="d1de8-116">*ObjectTypeId*</span></span> |<span data-ttu-id="d1de8-117">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="d1de8-117">Optional.</span></span> <span data-ttu-id="d1de8-118">Значение **типа Variant** , который указывает идентификатор GUID для поставщика тип объекта, не определена спецификацией OLE DB.</span><span class="sxs-lookup"><span data-stu-id="d1de8-118">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="d1de8-119">Этот параметр является обязательным, если *тип объекта* имеет значение **adPermObjProviderSpecific**; в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="d1de8-119">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="d1de8-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="d1de8-120">Remarks</span></span>

<span data-ttu-id="d1de8-121">Если поставщик поддерживает возвращает ошибку владельцы объектов, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="d1de8-121">An error will occur if the provider does not support returning object owners.</span></span>

