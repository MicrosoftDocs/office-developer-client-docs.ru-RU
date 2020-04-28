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
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="ff587-102">Метод GetObjectOwner (ADOX)</span><span class="sxs-lookup"><span data-stu-id="ff587-102">GetObjectOwner method (ADOX)</span></span>

<span data-ttu-id="ff587-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff587-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ff587-104">Возвращает владельца объекта в [каталоге](catalog-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="ff587-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ff587-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff587-105">Syntax</span></span>

<span data-ttu-id="ff587-106">*Owner* = *Каталог*владельца. GetObjectOwner (*имя_объекта*, *ObjectType* \[,*обжекттипеид*\])</span><span class="sxs-lookup"><span data-stu-id="ff587-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="ff587-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff587-107">Return value</span></span>

<span data-ttu-id="ff587-108">Возвращает **строковое** значение, задающее [имя](name-property-adox.md) [пользователя](user-object-adox.md) или [группы](group-object-adox.md) , которые являются владельцами объекта.</span><span class="sxs-lookup"><span data-stu-id="ff587-108">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="ff587-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff587-109">Parameters</span></span>

|<span data-ttu-id="ff587-110">Параметр</span><span class="sxs-lookup"><span data-stu-id="ff587-110">Parameter</span></span>|<span data-ttu-id="ff587-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ff587-111">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="ff587-112">*ObjectName*</span><span class="sxs-lookup"><span data-stu-id="ff587-112">*ObjectName*</span></span> |<span data-ttu-id="ff587-113">**Строковое** значение, задающее имя объекта, для которого требуется возвратить владельца.</span><span class="sxs-lookup"><span data-stu-id="ff587-113">A **String** value that specifies the name of the object for which to return the owner.</span></span>|
|<span data-ttu-id="ff587-114">*ObjectType*</span><span class="sxs-lookup"><span data-stu-id="ff587-114">*ObjectType*</span></span> |<span data-ttu-id="ff587-115">**Длинное** значение, которое может быть одной из констант [обжекттипинум](objecttypeenum.md) , которое указывает тип объекта, для которого требуется получить владельца.</span><span class="sxs-lookup"><span data-stu-id="ff587-115">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>|
|<span data-ttu-id="ff587-116">*обжекттипеид*</span><span class="sxs-lookup"><span data-stu-id="ff587-116">*ObjectTypeId*</span></span> |<span data-ttu-id="ff587-117">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="ff587-117">Optional.</span></span> <span data-ttu-id="ff587-118">Значение **Variant** , задающее GUID для типа объекта поставщика, не определенного СПЕЦИФИКАЦИЕЙ OLE DB.</span><span class="sxs-lookup"><span data-stu-id="ff587-118">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="ff587-119">Этот параметр является обязательным, если параметр *ObjectType* имеет значение **адпермобжпровидерспеЦифик**; в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="ff587-119">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>|

## <a name="remarks"></a><span data-ttu-id="ff587-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="ff587-120">Remarks</span></span>

<span data-ttu-id="ff587-121">Если поставщик не поддерживает возврат владельцев объекта, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="ff587-121">An error will occur if the provider does not support returning object owners.</span></span>

