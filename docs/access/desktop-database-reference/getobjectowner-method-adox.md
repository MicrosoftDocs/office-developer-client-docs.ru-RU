---
title: Метод GetObjectOwner (ADOX)
TOCTitle: GetObjectOwner method (ADOX)
ms:assetid: 716dd49a-8663-3f7a-32a3-0be353aea506
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249451(v=office.15)
ms:contentKeyID: 48545585
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1a37b0f341c849358b649c2222df2955fd88f5d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927819"
---
# <a name="getobjectowner-method-adox"></a><span data-ttu-id="399a5-102">Метод GetObjectOwner (ADOX)</span><span class="sxs-lookup"><span data-stu-id="399a5-102">GetObjectOwner method (ADOX)</span></span>


<span data-ttu-id="399a5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="399a5-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="399a5-104">Возвращает владельца объекта в [каталоге](catalog-object-adox.md).</span><span class="sxs-lookup"><span data-stu-id="399a5-104">Returns the owner of an object in a [Catalog](catalog-object-adox.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="399a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="399a5-105">Syntax</span></span>

<span data-ttu-id="399a5-106">*Владелец* = *каталога*. GetObjectOwner (*имя объекта*, *ObjectType* \[,*ObjectTypeId*\])</span><span class="sxs-lookup"><span data-stu-id="399a5-106">*Owner* = *Catalog*.GetObjectOwner(*ObjectName*, *ObjectType* \[,*ObjectTypeId*\])</span></span>

## <a name="return-value"></a><span data-ttu-id="399a5-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="399a5-107">Return value</span></span>

<span data-ttu-id="399a5-108">Возвращает **строковое** значение, задающее [имя](name-property-adox.md) [пользователя](user-object-adox.md) или [группы](group-object-adox.md) , которому принадлежит объект.</span><span class="sxs-lookup"><span data-stu-id="399a5-108">Returns a **String** value that specifies the [Name](name-property-adox.md) of the [User](user-object-adox.md) or [Group](group-object-adox.md) that owns the object.</span></span>

## <a name="parameters"></a><span data-ttu-id="399a5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="399a5-109">Parameters</span></span>

  - <span data-ttu-id="399a5-110">*Имя объекта*</span><span class="sxs-lookup"><span data-stu-id="399a5-110">*ObjectName*</span></span>

  - <span data-ttu-id="399a5-111">**Строковое** значение, указывающее имя объекта, для которого возвращаются владельца.</span><span class="sxs-lookup"><span data-stu-id="399a5-111">A **String** value that specifies the name of the object for which to return the owner.</span></span>

  - <span data-ttu-id="399a5-112">*Тип объекта*</span><span class="sxs-lookup"><span data-stu-id="399a5-112">*ObjectType*</span></span>

  - <span data-ttu-id="399a5-113">**Длинное целое** значение, который может быть одной из констант [ObjectTypeEnum](objecttypeenum.md) , указывает тип объекта, для которого необходимо получить владельца.</span><span class="sxs-lookup"><span data-stu-id="399a5-113">A **Long** value which can be one of the [ObjectTypeEnum](objecttypeenum.md) constants, that specifies the type of the object for which to get the owner.</span></span>

  - <span data-ttu-id="399a5-114">*ObjectTypeId*</span><span class="sxs-lookup"><span data-stu-id="399a5-114">*ObjectTypeId*</span></span>

  - <span data-ttu-id="399a5-115">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="399a5-115">Optional.</span></span> <span data-ttu-id="399a5-116">Значение **типа Variant** , который указывает идентификатор GUID для поставщика тип объекта, не определена спецификацией OLE DB.</span><span class="sxs-lookup"><span data-stu-id="399a5-116">A **Variant** value that specifies the GUID for a provider object type not defined by the OLE DB specification.</span></span> <span data-ttu-id="399a5-117">Этот параметр является обязательным, если *тип объекта* имеет значение **adPermObjProviderSpecific**; в противном случае он не используется.</span><span class="sxs-lookup"><span data-stu-id="399a5-117">This parameter is required if *ObjectType* is set to **adPermObjProviderSpecific**; otherwise, it is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="399a5-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="399a5-118">Remarks</span></span>

<span data-ttu-id="399a5-119">Если поставщик поддерживает возвращает ошибку владельцы объектов, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="399a5-119">An error will occur if the provider does not support returning object owners.</span></span>

