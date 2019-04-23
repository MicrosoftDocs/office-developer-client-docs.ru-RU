---
title: Свойство LockType (ADO)
TOCTitle: LockType property (ADO)
ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15)
ms:contentKeyID: 48543589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d12946a90d61a941bf5ef7d479970c8c96e074f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289845"
---
# <a name="locktype-property-ado"></a><span data-ttu-id="89fa7-102">Свойство LockType (ADO)</span><span class="sxs-lookup"><span data-stu-id="89fa7-102">LockType property (ADO)</span></span>


<span data-ttu-id="89fa7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="89fa7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="89fa7-104">Указывает тип блокировок, помещаемых в записи во время редактирования.</span><span class="sxs-lookup"><span data-stu-id="89fa7-104">Indicates the type of locks placed on records during editing.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="89fa7-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="89fa7-105">Settings and return values</span></span>

<span data-ttu-id="89fa7-106">Задает или возвращает значение [LockTypeEnum](locktypeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="89fa7-106">Sets or returns a [LockTypeEnum](locktypeenum.md) value.</span></span> <span data-ttu-id="89fa7-107">Значение по умолчанию — **адлоккреадонли**.</span><span class="sxs-lookup"><span data-stu-id="89fa7-107">The default value is **adLockReadOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="89fa7-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="89fa7-108">Remarks</span></span>

<span data-ttu-id="89fa7-109">Задайте свойство **LockType** перед открытием объекта [Recordset](recordset-object-ado.md) , чтобы указать тип блокировки, который должен использоваться поставщиком при его открытии.</span><span class="sxs-lookup"><span data-stu-id="89fa7-109">Set the **LockType** property before opening a [Recordset](recordset-object-ado.md) to specify what type of locking the provider should use when opening it.</span></span> <span data-ttu-id="89fa7-110">Прочитайте свойство, чтобы возвратить тип блокировки, используемой в открытом объекте **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="89fa7-110">Read the property to return the type of locking in use on an open **Recordset** object.</span></span>

<span data-ttu-id="89fa7-111">Поставщики могут не поддерживать все типы блокировок.</span><span class="sxs-lookup"><span data-stu-id="89fa7-111">Providers may not support all lock types.</span></span> <span data-ttu-id="89fa7-112">Если поставщик не поддерживает запрошенный параметр **LockType** , он заменит другой тип блокировки.</span><span class="sxs-lookup"><span data-stu-id="89fa7-112">If a provider cannot support the requested **LockType** setting, it will substitute another type of locking.</span></span> <span data-ttu-id="89fa7-113">Чтобы определить существующие функциональные возможности блокировки, доступные в объекте **Recordset** , используйте метод [](supports-method-ado.md) Supports с **адупдате** и **адупдатебатч**.</span><span class="sxs-lookup"><span data-stu-id="89fa7-113">To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**.</span></span>

<span data-ttu-id="89fa7-114">Параметр **адлоккпессимистик** не поддерживается, если для свойства [CursorLocation](cursorlocation-property-ado.md) задано значение **адусеклиент**.</span><span class="sxs-lookup"><span data-stu-id="89fa7-114">The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span> <span data-ttu-id="89fa7-115">Если задано неподдерживаемое значение, ошибка не будет возникать; Вместо этого будет использоваться ближайшее поддерживаемое **LockType** .</span><span class="sxs-lookup"><span data-stu-id="89fa7-115">If an unsupported value is set, then no error will result; the closest supported **LockType** will be used instead.</span></span>

<span data-ttu-id="89fa7-116">Свойство **LockType** доступно для чтения и записи, когда **набор записей** закрывается и только для чтения, когда он открыт.</span><span class="sxs-lookup"><span data-stu-id="89fa7-116">The **LockType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="89fa7-117">**Использование удаленной службы данных** При использовании в объекте Recordset на стороне клиента для свойства **LockType** можно задать только значение **адлоккбатчоптимистик**.</span><span class="sxs-lookup"><span data-stu-id="89fa7-117">**Remote Data Service Usage**When used on a client-side Recordset object, the **LockType** property can only be set to **adLockBatchOptimistic**.</span></span>

