---
title: LockType Property (ADO)
TOCTitle: LockType Property (ADO)
ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15)
ms:contentKeyID: 48543589
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d1740f42fae3485d88a4820081621f7f2483c51
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482409"
---
# <a name="locktype-property-ado"></a><span data-ttu-id="b3801-102">LockType Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="b3801-102">LockType Property (ADO)</span></span>


<span data-ttu-id="b3801-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b3801-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b3801-104">Указывает тип блокировки записей во время редактирования.</span><span class="sxs-lookup"><span data-stu-id="b3801-104">Indicates the type of locks placed on records during editing.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b3801-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="b3801-105">Settings and Return Values</span></span>

<span data-ttu-id="b3801-106">Задает или возвращает значение [LockTypeEnum](locktypeenum.md) .</span><span class="sxs-lookup"><span data-stu-id="b3801-106">Sets or returns a [LockTypeEnum](locktypeenum.md) value.</span></span> <span data-ttu-id="b3801-107">Значение по умолчанию — **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="b3801-107">The default value is **adLockReadOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3801-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="b3801-108">Remarks</span></span>

<span data-ttu-id="b3801-109">Присвойте свойству **LockType для** перед открытием [набора записей](recordset-object-ado.md) , чтобы указать, какой блокировки поставщика следует использовать при открытии его.</span><span class="sxs-lookup"><span data-stu-id="b3801-109">Set the **LockType** property before opening a [Recordset](recordset-object-ado.md) to specify what type of locking the provider should use when opening it.</span></span> <span data-ttu-id="b3801-110">Чтение свойства для возвращения типа блокировки используется open объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="b3801-110">Read the property to return the type of locking in use on an open **Recordset** object.</span></span>

<span data-ttu-id="b3801-111">Поставщики могут не поддерживать все типы блокировки.</span><span class="sxs-lookup"><span data-stu-id="b3801-111">Providers may not support all lock types.</span></span> <span data-ttu-id="b3801-112">Если поставщик не поддерживает запрошенный **LockType для** параметра, он будет заменить другой тип блокировки.</span><span class="sxs-lookup"><span data-stu-id="b3801-112">If a provider cannot support the requested **LockType** setting, it will substitute another type of locking.</span></span> <span data-ttu-id="b3801-113">Чтобы определить фактический блокировки функциональные возможности, доступные в объекте **набора записей** , используйте метод [поддерживает](supports-method-ado.md) с **adUpdate** и **adUpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="b3801-113">To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**.</span></span>

<span data-ttu-id="b3801-114">Параметр **adLockPessimistic** не поддерживается, если свойство [CursorLocation](cursorlocation-property-ado.md) имеет значение **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="b3801-114">The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span> <span data-ttu-id="b3801-115">Если задано значение не поддерживается, сообщение об ошибке не приведет к; ближайший поддерживаемый **LockType для** будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="b3801-115">If an unsupported value is set, then no error will result; the closest supported **LockType** will be used instead.</span></span>

<span data-ttu-id="b3801-116">Свойство **LockType для** чтения и записи при выполняется **записей** закрытой и только для чтения при открытии.</span><span class="sxs-lookup"><span data-stu-id="b3801-116">The **LockType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="b3801-117">**Службы удаленных данных об использовании** При использовании в объект набора записей со стороны клиента, свойство **LockType для** может устанавливаться только для **adLockBatchOptimistic**.</span><span class="sxs-lookup"><span data-stu-id="b3801-117">**Remote Data Service Usage**When used on a client-side Recordset object, the **LockType** property can only be set to **adLockBatchOptimistic**.</span></span>

