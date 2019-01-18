---
title: Свойство TableDef.ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 9f38616a-41ee-cbd1-9e29-da436b258e08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198366(v=office.15)
ms:contentKeyID: 48546682
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f2c45aa1bd6f470b342ffec51f2affd39c7cb552
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710484"
---
# <a name="tabledefvalidationtext-property-dao"></a><span data-ttu-id="c8868-102">Свойство TableDef.ValidationText (DAO)</span><span class="sxs-lookup"><span data-stu-id="c8868-102">TableDef.ValidationText property (DAO)</span></span>


<span data-ttu-id="c8868-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8868-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c8868-104">Задает или возвращает значение, указывающее, текст сообщения, приложение, если значение **поля** объекта не удовлетворяют правило проверки, указанного идентификатором **условие на значение** свойства поля (только для рабочих областей Microsoft Access) .</span><span class="sxs-lookup"><span data-stu-id="c8868-104">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="c8868-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="c8868-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8868-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8868-106">Syntax</span></span>

<span data-ttu-id="c8868-107">*выражение* . Сообщение об ошибке</span><span class="sxs-lookup"><span data-stu-id="c8868-107">*expression* .ValidationText</span></span>

<span data-ttu-id="c8868-108">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="c8868-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8868-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="c8868-109">Remarks</span></span>

<span data-ttu-id="c8868-110">Для объекта **[TableDef](tabledef-object-dao.md)** значение этого свойства доступно только для чтения для связанной таблицы, а также чтения и записи для базовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="c8868-110">For a **[TableDef](tabledef-object-dao.md)** object, this property setting is read-only for a linked table and read/write for a base table.</span></span>

