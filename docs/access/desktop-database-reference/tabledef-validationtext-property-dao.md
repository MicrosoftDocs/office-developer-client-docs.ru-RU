---
title: Свойство TableDef. ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 9f38616a-41ee-cbd1-9e29-da436b258e08
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198366(v=office.15)
ms:contentKeyID: 48546682
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f2c45aa1bd6f470b342ffec51f2affd39c7cb552
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314247"
---
# <a name="tabledefvalidationtext-property-dao"></a><span data-ttu-id="c2cd6-102">Свойство TableDef. ValidationText (DAO)</span><span class="sxs-lookup"><span data-stu-id="c2cd6-102">TableDef.ValidationText property (DAO)</span></span>


<span data-ttu-id="c2cd6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2cd6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c2cd6-104">Задает или возвращает значение, определяющее текст сообщения, которое отображает ваше приложение, если значение объекта **Field** не удовлетворяют правилу проверки, задаваемому настройкой параметра **ValidationRule** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="c2cd6-104">Sets or returns a value that specifies the text of the message that your application displays if the value of a **Field** object doesn't satisfy the validation rule specified by the **ValidationRule** property setting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="c2cd6-105">Для чтения и записи, **String**.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-105">Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2cd6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2cd6-106">Syntax</span></span>

<span data-ttu-id="c2cd6-107">*Expression* . ValidationText</span><span class="sxs-lookup"><span data-stu-id="c2cd6-107">*expression* .ValidationText</span></span>

<span data-ttu-id="c2cd6-108">*выражение*: переменная, представляющая объект **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2cd6-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2cd6-109">Remarks</span></span>

<span data-ttu-id="c2cd6-110">Для объекта **[tabledef](tabledef-object-dao.md)** это свойство доступно только для чтения для связанной таблицы, а для базовой таблицы — для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c2cd6-110">For a **[TableDef](tabledef-object-dao.md)** object, this property setting is read-only for a linked table and read/write for a base table.</span></span>

