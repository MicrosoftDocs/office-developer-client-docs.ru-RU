---
title: Свойство TableDef.ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 9f38616a-41ee-cbd1-9e29-da436b258e08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198366(v=office.15)
ms:contentKeyID: 48546682
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b90c2fe3d27dea2f90261cda66e0cd0460349482
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921910"
---
# <a name="tabledefvalidationtext-property-dao"></a><span data-ttu-id="16825-102">Свойство TableDef.ValidationText (DAO)</span><span class="sxs-lookup"><span data-stu-id="16825-102">TableDef.ValidationText property (DAO)</span></span>


<span data-ttu-id="16825-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="16825-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="16825-104">Задает или возвращает значение, указывающее, текст сообщения, приложение, если значение **поля** объекта не удовлетворяют правило проверки, указанного идентификатором **условие на значение** свойства поля (только для рабочих областей Microsoft Access) .</span><span class="sxs-lookup"><span data-stu-id="16825-104">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="16825-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="16825-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="16825-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16825-106">Syntax</span></span>

<span data-ttu-id="16825-107">*выражение* . Сообщение об ошибке</span><span class="sxs-lookup"><span data-stu-id="16825-107">*expression* .ValidationText</span></span>

<span data-ttu-id="16825-108">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="16825-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="16825-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="16825-109">Remarks</span></span>

<span data-ttu-id="16825-110">Для объекта **[TableDef](tabledef-object-dao.md)** значение этого свойства доступно только для чтения для связанной таблицы, а также чтения и записи для базовой таблицы.</span><span class="sxs-lookup"><span data-stu-id="16825-110">For a **[TableDef](tabledef-object-dao.md)** object, this property setting is read-only for a linked table and read/write for a base table.</span></span>

