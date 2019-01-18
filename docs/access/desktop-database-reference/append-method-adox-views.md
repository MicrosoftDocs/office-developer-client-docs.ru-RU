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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716156"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="43a17-102">Метод Append (Views в ADOX)</span><span class="sxs-lookup"><span data-stu-id="43a17-102">Append method (ADOX Views)</span></span>

<span data-ttu-id="43a17-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="43a17-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="43a17-104">Создает новый объект [представления](view-object-adox.md) и добавляет его в коллекцию [представлений](views-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="43a17-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a17-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43a17-105">Syntax</span></span>

<span data-ttu-id="43a17-106">*Представления*. Добавьте*имя*, *команда*</span><span class="sxs-lookup"><span data-stu-id="43a17-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="43a17-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="43a17-107">Parameters</span></span>

|<span data-ttu-id="43a17-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="43a17-108">Parameter</span></span>|<span data-ttu-id="43a17-109">Описание</span><span class="sxs-lookup"><span data-stu-id="43a17-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="43a17-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="43a17-110">*Name*</span></span> |<span data-ttu-id="43a17-111">**Строковое** значение, задающее имя представления для создания.</span><span class="sxs-lookup"><span data-stu-id="43a17-111">A **String** value that specifies the name of the view to create.</span></span>|
|<span data-ttu-id="43a17-112">*Command*</span><span class="sxs-lookup"><span data-stu-id="43a17-112">*Command*</span></span> |<span data-ttu-id="43a17-113">Объект ADO [команды](command-object-ado.md) , представляющий представление для создания.</span><span class="sxs-lookup"><span data-stu-id="43a17-113">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>|

## <a name="remarks"></a><span data-ttu-id="43a17-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="43a17-114">Remarks</span></span>

<span data-ttu-id="43a17-115">Создает новое представление источника данных с именем и атрибуты, указанные в объекте **команды** .</span><span class="sxs-lookup"><span data-stu-id="43a17-115">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="43a17-116">Если текст команды, который пользователь вводит представляет процедуры, а не как представление, поведение зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="43a17-116">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider.</span></span> <span data-ttu-id="43a17-117">**Добавление** завершится ошибкой, если поставщик не поддерживает сохранение команды.</span><span class="sxs-lookup"><span data-stu-id="43a17-117">**Append** will fail if the provider does not support persisting commands.</span></span>

> [!NOTE]
> <span data-ttu-id="43a17-118">При использовании поставщика OLE DB для Microsoft Jet, коллекции **представлений** метод **Append** позволит можно использовать для определения **процедуры** , а не в **представлении** с помощью параметра *командной* .</span><span class="sxs-lookup"><span data-stu-id="43a17-118">When using the OLE DB Provider for Microsoft Jet, the **Views** collection **Append** method will allow you to specify a **Procedure** rather than a **View** in the *Command* parameter.</span></span> <span data-ttu-id="43a17-119">**Процедуры** добавляются к источнику данных и добавляются в коллекцию **представлений** .</span><span class="sxs-lookup"><span data-stu-id="43a17-119">The **Procedure** will be added to the data source and will be added to the **Views** collection.</span></span> <span data-ttu-id="43a17-120">После **добавления**при обновлении семейств сайтов **процедуры** и **представления** **процедуры** больше не будет находиться в коллекции **представлений** и будет отображаться в коллекции **процедур** .</span><span class="sxs-lookup"><span data-stu-id="43a17-120">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **Procedure** will no longer be in the **Views** collection and will appear in the **Procedures** collection.</span></span>


