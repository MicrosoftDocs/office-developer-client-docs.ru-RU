---
title: CursorLocation Property (ADO)
TOCTitle: CursorLocation Property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9805b032a0e1a203d2a4057fb74757826a2a47b4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481568"
---
# <a name="cursorlocation-property-ado"></a><span data-ttu-id="d2455-102">CursorLocation Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="d2455-102">CursorLocation Property (ADO)</span></span>


<span data-ttu-id="d2455-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2455-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d2455-104">Указывает расположение службы курсора.</span><span class="sxs-lookup"><span data-stu-id="d2455-104">Indicates the location of the cursor service.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="d2455-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="d2455-105">Settings And Return Values</span></span>

<span data-ttu-id="d2455-106">Задает или возвращает значение типа **Long** , может быть установлено одно из значений [CursorLocationEnum](cursorlocationenum.md) .</span><span class="sxs-lookup"><span data-stu-id="d2455-106">Sets or returns a **Long** value that can be set to one of the [CursorLocationEnum](cursorlocationenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2455-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="d2455-107">Remarks</span></span>

<span data-ttu-id="d2455-108">Это свойство можно выбрать одну из различных библиотек курсора, доступной для поставщика.</span><span class="sxs-lookup"><span data-stu-id="d2455-108">This property allows you to choose between various cursor libraries accessible to the provider.</span></span> <span data-ttu-id="d2455-109">Как правило вы можете выбрать одну с помощью библиотеки курсор на стороне клиента, либо, расположенного на сервере.</span><span class="sxs-lookup"><span data-stu-id="d2455-109">Usually, you can choose between using a client-side cursor library or one that is located on the server.</span></span>

<span data-ttu-id="d2455-110">Установка этого свойства влияет только после установки свойства подключений.</span><span class="sxs-lookup"><span data-stu-id="d2455-110">This property setting affects connections established only after the property has been set.</span></span> <span data-ttu-id="d2455-111">Изменение свойства **CursorLocation** не влияет на существующие подключения.</span><span class="sxs-lookup"><span data-stu-id="d2455-111">Changing the **CursorLocation** property has no effect on existing connections.</span></span>

<span data-ttu-id="d2455-112">Курсоры, возвращенный методом [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) наследовать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d2455-112">Cursors returned by the [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) method inherit this setting.</span></span> <span data-ttu-id="d2455-113">Объекты **набора записей** автоматически наследуют их связанного подключения этот параметр.</span><span class="sxs-lookup"><span data-stu-id="d2455-113">**Recordset** objects will automatically inherit this setting from their associated connections.</span></span>

<span data-ttu-id="d2455-114">Это свойство является чтение и запись на [подключение](connection-object-ado.md) или закрытой [записей](recordset-object-ado.md)и только для чтения на открытие **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="d2455-114">This property is read/write on a [Connection](connection-object-ado.md) or a closed [Recordset](recordset-object-ado.md), and read-only on an open **Recordset**.</span></span>

<span data-ttu-id="d2455-115">**Службы удаленных данных об использовании** При использовании на стороне клиента **записей** или объект **подключения** свойства **CursorLocation** может устанавливаться только для **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="d2455-115">**Remote Data Service Usage**When used on a client-side **Recordset** or **Connection** object, the **CursorLocation** property can only be set to **adUseClient**.</span></span>

