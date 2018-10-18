---
title: GetObjectOwner Method (ADOX)
TOCTitle: GetObjectOwner Method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e6c2432370f2480484cf1165249bc8573b27372
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603114"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="a044f-102">GetObjectOwner Method (ADOX)</span><span class="sxs-lookup"><span data-stu-id="a044f-102">GetObjectOwner Method (ADOX)</span></span>


<span data-ttu-id="a044f-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a044f-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="a044f-104">Возвращает владельца объекта в [каталоге](catalog-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="a044f-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a044f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a044f-105">Syntax</span></span>

<span data-ttu-id="a044f-106">*Владелец* = *каталога*. GetObjectOwner (*имя объекта*, *ObjectType* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="a044f-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

<span data-ttu-id="a044f-107"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="a044f-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="a044f-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a044f-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="a044f-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a044f-109">Return value</span></span>
>>>>>>> <span data-ttu-id="a044f-110">master</span><span class="sxs-lookup"><span data-stu-id="a044f-110">master</span></span>

<span data-ttu-id="a044f-111">Возвращает **строковое** значение, задающее [имя](name-property-adox.md) [пользователя](user-object-adox.md) или [группы](group-object-adox.md) , которому принадлежит объект.</span><span class="sxs-lookup"><span data-stu-id="a044f-111">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="a044f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="a044f-112">Parameters</span></span>

  - <span data-ttu-id="a044f-113">*Имя объекта*</span><span class="sxs-lookup"><span data-stu-id="a044f-113">*ObjectName*</span></span>

  - <span data-ttu-id="a044f-114">**Строковое** значение, указывающее имя объекта, для которого возвращаются владельца.</span><span class="sxs-lookup"><span data-stu-id="a044f-114">A **String** value that specifies the name of the object for which to return the owner.</span></span>

  - <span data-ttu-id="a044f-115">*Тип объекта*</span><span class="sxs-lookup"><span data-stu-id="a044f-115">*ObjectType*</span></span>

  - <span data-ttu-id="a044f-116">**Длинное целое** значение, который может быть одной из констант [ObjectTypeEnum](objecttypeenum.md) , указывает тип объекта, для которого необходимо получить владельца.</span><span class="sxs-lookup"><span data-stu-id="a044f-116">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>

  - <span data-ttu-id="a044f-117">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="a044f-117">*ObjectTypeId*</span></span>

  - <span data-ttu-id="a044f-118">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="a044f-118">Optional.</span></span> <span data-ttu-id="a044f-119">Значение **типа Variant** , который указывает идентификатор GUID для поставщика тип объекта, не определена спецификацией OLE DB.</span><span class="sxs-lookup"><span data-stu-id="a044f-119">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="a044f-120">Этот параметр является обязательным, если *тип объекта* имеет значение **adPermObjProviderSpecific**; в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="a044f-120">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="a044f-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="a044f-121">Remarks</span></span>

<span data-ttu-id="a044f-122">Если поставщик поддерживает возвращает ошибку владельцы объектов, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="a044f-122">An error will occur if the provider does not support returning object owners.</span></span>

