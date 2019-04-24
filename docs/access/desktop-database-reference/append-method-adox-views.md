---
title: Метод Append (Views в ADOX)
TOCTitle: Append method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9e1a6e14542f267af6a9f5bc58bb2d75a11aac77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297048"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="074d2-102">Метод Append (Views в ADOX)</span><span class="sxs-lookup"><span data-stu-id="074d2-102">Append method (ADOX Views)</span></span>

<span data-ttu-id="074d2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="074d2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="074d2-104">Создает новый объект [View](view-object-adox.md) и добавляет его в коллекцию views [](views-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="074d2-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="074d2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="074d2-105">Syntax</span></span>

<span data-ttu-id="074d2-106">*Представления*. *Имя*для добавления, *команда*</span><span class="sxs-lookup"><span data-stu-id="074d2-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="074d2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="074d2-107">Parameters</span></span>

|<span data-ttu-id="074d2-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="074d2-108">Parameter</span></span>|<span data-ttu-id="074d2-109">Описание</span><span class="sxs-lookup"><span data-stu-id="074d2-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="074d2-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="074d2-110">*Name*</span></span> |<span data-ttu-id="074d2-111">**Строковое** значение, задающее имя создаваемого представления.</span><span class="sxs-lookup"><span data-stu-id="074d2-111">A **String** value that specifies the name of the view to create.</span></span>|
|<span data-ttu-id="074d2-112">*Command*</span><span class="sxs-lookup"><span data-stu-id="074d2-112">*Command*</span></span> |<span data-ttu-id="074d2-113">Объект [команды](command-object-ado.md) ADO, представляющий представление, которое требуется создать.</span><span class="sxs-lookup"><span data-stu-id="074d2-113">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>|

## <a name="remarks"></a><span data-ttu-id="074d2-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="074d2-114">Remarks</span></span>

<span data-ttu-id="074d2-115">Создает новое представление в источнике данных с именем и атрибутами, указанными в объекте **Command** .</span><span class="sxs-lookup"><span data-stu-id="074d2-115">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="074d2-116">Если текст команды, который указывает пользователь, представляет процедуру, а не представление, поведение зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="074d2-116">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider.</span></span> <span data-ttu-id="074d2-117">Если поставщик не поддерживает хранимые команды, **append** завершится с ошибками.</span><span class="sxs-lookup"><span data-stu-id="074d2-117">**Append** will fail if the provider does not support persisting commands.</span></span>

> [!NOTE]
> <span data-ttu-id="074d2-118">При использовании поставщика OLE DB для Microsoft Jet метод **append** коллекции **views** позволяет указать **процедуру** , а не **представление** в параметре *Command* .</span><span class="sxs-lookup"><span data-stu-id="074d2-118">When using the OLE DB Provider for Microsoft Jet, the **Views** collection **Append** method will allow you to specify a **Procedure** rather than a **View** in the *Command* parameter.</span></span> <span data-ttu-id="074d2-119">**Процедура** будет добавлена в источник данных и будет добавлена в коллекцию **views** .</span><span class="sxs-lookup"><span data-stu-id="074d2-119">The **Procedure** will be added to the data source and will be added to the **Views** collection.</span></span> <span data-ttu-id="074d2-120">После **добавления**, если коллекции **процедур** и **представлений** обновляются, **процедура** больше не будет находиться в коллекции Views и будет отображаться \*\*\*\* в коллекции **процедур** .</span><span class="sxs-lookup"><span data-stu-id="074d2-120">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **Procedure** will no longer be in the **Views** collection and will appear in the **Procedures** collection.</span></span>


