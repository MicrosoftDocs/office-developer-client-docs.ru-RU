---
title: Свойство CursorLocation (ADO)
TOCTitle: CursorLocation property (ADO)
ms:assetid: 8a048bd4-ae25-a555-1c07-14364b7e6560
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249606(v=office.15)
ms:contentKeyID: 48546182
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25fd81acee3c541c8a3f315f96fa69241272a655
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295222"
---
# <a name="cursorlocation-property-ado"></a><span data-ttu-id="76c4a-102">Свойство CursorLocation (ADO)</span><span class="sxs-lookup"><span data-stu-id="76c4a-102">CursorLocation property (ADO)</span></span>


<span data-ttu-id="76c4a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="76c4a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="76c4a-104">Указывает расположение службы курсора.</span><span class="sxs-lookup"><span data-stu-id="76c4a-104">Indicates the location of the cursor service.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="76c4a-105">Параметры и возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="76c4a-105">Settings And Return Values</span></span>

<span data-ttu-id="76c4a-106">Задает или возвращает **длинное** значение, которое можно установить как одно из [значений CursorLocationEnum.](cursorlocationenum.md)</span><span class="sxs-lookup"><span data-stu-id="76c4a-106">Sets or returns a **Long** value that can be set to one of the [CursorLocationEnum](cursorlocationenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="76c4a-107">Заметки</span><span class="sxs-lookup"><span data-stu-id="76c4a-107">Remarks</span></span>

<span data-ttu-id="76c4a-108">Это свойство позволяет выбрать различные библиотеки курсоров, доступные поставщику.</span><span class="sxs-lookup"><span data-stu-id="76c4a-108">This property allows you to choose between various cursor libraries accessible to the provider.</span></span> <span data-ttu-id="76c4a-109">Обычно можно выбрать клиентскую библиотеку курсоров или библиотеку, расположенную на сервере.</span><span class="sxs-lookup"><span data-stu-id="76c4a-109">Usually, you can choose between using a client-side cursor library or one that is located on the server.</span></span>

<span data-ttu-id="76c4a-110">Этот параметр свойства влияет на подключения, установленные только после установки свойства.</span><span class="sxs-lookup"><span data-stu-id="76c4a-110">This property setting affects connections established only after the property has been set.</span></span> <span data-ttu-id="76c4a-111">Изменение свойства **CursorLocation** не влияет на существующие подключения.</span><span class="sxs-lookup"><span data-stu-id="76c4a-111">Changing the **CursorLocation** property has no effect on existing connections.</span></span>

<span data-ttu-id="76c4a-112">Курсоры, возвращенные методом [Execute,](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) наследуют этот параметр.</span><span class="sxs-lookup"><span data-stu-id="76c4a-112">Cursors returned by the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method inherit this setting.</span></span> <span data-ttu-id="76c4a-113">**Объекты recordset** автоматически наследуют этот параметр от связанных подключений.</span><span class="sxs-lookup"><span data-stu-id="76c4a-113">**Recordset** objects will automatically inherit this setting from their associated connections.</span></span>

<span data-ttu-id="76c4a-114">Это свойство для чтения и записи в [connection](connection-object-ado.md) или закрытом наборе [записей](recordset-object-ado.md)и только для чтения в открытом **наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="76c4a-114">This property is read/write on a [Connection](connection-object-ado.md) or a closed [Recordset](recordset-object-ado.md), and read-only on an open **Recordset**.</span></span>

<span data-ttu-id="76c4a-115">**Использование удаленной службы данных** При клиентском объекте **Recordset** или **Connection** свойство **CursorLocation** можно установить только в **adUseClient.**</span><span class="sxs-lookup"><span data-stu-id="76c4a-115">**Remote Data Service Usage** When used on a client-side **Recordset** or **Connection** object, the **CursorLocation** property can only be set to **adUseClient**.</span></span>

