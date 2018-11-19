---
title: Свойство CursorLocation (ADO)
TOCTitle: CursorLocation property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 874662585292b9d9a9b2bc53f5b6fe5178e3517b
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025849"
---
# <a name="cursorlocation-property-ado"></a><span data-ttu-id="9c880-102">Свойство CursorLocation (ADO)</span><span class="sxs-lookup"><span data-stu-id="9c880-102">CursorLocation property (ADO)</span></span>


<span data-ttu-id="9c880-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9c880-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9c880-104">Указывает расположение службы курсора.</span><span class="sxs-lookup"><span data-stu-id="9c880-104">Indicates the location of the cursor service.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="9c880-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="9c880-105">Settings And Return Values</span></span>

<span data-ttu-id="9c880-106">Задает или возвращает значение типа **Long** , может быть установлено одно из значений [CursorLocationEnum](cursorlocationenum.md) .</span><span class="sxs-lookup"><span data-stu-id="9c880-106">Sets or returns a **Long** value that can be set to one of the [CursorLocationEnum](cursorlocationenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c880-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="9c880-107">Remarks</span></span>

<span data-ttu-id="9c880-108">Это свойство можно выбрать одну из различных библиотек курсора, доступной для поставщика.</span><span class="sxs-lookup"><span data-stu-id="9c880-108">This property allows you to choose between various cursor libraries accessible to the provider.</span></span> <span data-ttu-id="9c880-109">Как правило вы можете выбрать одну с помощью библиотеки курсор на стороне клиента, либо, расположенного на сервере.</span><span class="sxs-lookup"><span data-stu-id="9c880-109">Usually, you can choose between using a client-side cursor library or one that is located on the server.</span></span>

<span data-ttu-id="9c880-110">Установка этого свойства влияет только после установки свойства подключений.</span><span class="sxs-lookup"><span data-stu-id="9c880-110">This property setting affects connections established only after the property has been set.</span></span> <span data-ttu-id="9c880-111">Изменение свойства **CursorLocation** не влияет на существующие подключения.</span><span class="sxs-lookup"><span data-stu-id="9c880-111">Changing the **CursorLocation** property has no effect on existing connections.</span></span>

<span data-ttu-id="9c880-112">Курсоры, возвращенный методом [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) наследовать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9c880-112">Cursors returned by the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method inherit this setting.</span></span> <span data-ttu-id="9c880-113">Объекты **набора записей** автоматически наследуют их связанного подключения этот параметр.</span><span class="sxs-lookup"><span data-stu-id="9c880-113">**Recordset** objects will automatically inherit this setting from their associated connections.</span></span>

<span data-ttu-id="9c880-114">Это свойство является чтение и запись на [подключение](connection-object-ado.md) или закрытой [записей](recordset-object-ado.md)и только для чтения на открытие **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="9c880-114">This property is read/write on a [Connection](connection-object-ado.md) or a closed [Recordset](recordset-object-ado.md), and read-only on an open **Recordset**.</span></span>

<span data-ttu-id="9c880-115">**Службы удаленных данных об использовании** При использовании на стороне клиента **записей** или объект **подключения** свойства **CursorLocation** может устанавливаться только для **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="9c880-115">**Remote Data Service Usage**When used on a client-side **Recordset** or **Connection** object, the **CursorLocation** property can only be set to **adUseClient**.</span></span>

