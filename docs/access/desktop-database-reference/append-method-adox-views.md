---
title: Метод Append (коллекция Views в ADOX)
TOCTitle: Append method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ccba425e74321f4ab760e9ddc4a722295290ffd1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925158"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="15987-102">Метод Append (коллекция Views в ADOX)</span><span class="sxs-lookup"><span data-stu-id="15987-102">Append method (ADOX Views)</span></span>


<span data-ttu-id="15987-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="15987-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="15987-104">Создает новый объект [представления](view-object-adox.md) и добавляет его в коллекцию [представлений](views-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="15987-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="15987-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="15987-105">Syntax</span></span>

<span data-ttu-id="15987-106">*Представления*. Добавьте*имя*, *команда*</span><span class="sxs-lookup"><span data-stu-id="15987-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="15987-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="15987-107">Parameters</span></span>

  - <span data-ttu-id="15987-108">*Имя*</span><span class="sxs-lookup"><span data-stu-id="15987-108">*Name*</span></span>

  - <span data-ttu-id="15987-109">**Строковое** значение, задающее имя представления для создания.</span><span class="sxs-lookup"><span data-stu-id="15987-109">A **String** value that specifies the name of the view to create.</span></span>

  - <span data-ttu-id="15987-110">*Команда*</span><span class="sxs-lookup"><span data-stu-id="15987-110">*Command*</span></span>

  - <span data-ttu-id="15987-111">Объект ADO [команды](command-object-ado.md) , представляющий представление для создания.</span><span class="sxs-lookup"><span data-stu-id="15987-111">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>

## <a name="remarks"></a><span data-ttu-id="15987-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="15987-112">Remarks</span></span>

<span data-ttu-id="15987-113">Создает новое представление источника данных с именем и атрибуты, указанные в объекте **команды** .</span><span class="sxs-lookup"><span data-stu-id="15987-113">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="15987-114">Если текст команды, который пользователь вводит представляет процедуры, а не как представление, поведение зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="15987-114">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider.</span></span> <span data-ttu-id="15987-115">**Добавление** завершится ошибкой, если поставщик не поддерживает сохранение команды.</span><span class="sxs-lookup"><span data-stu-id="15987-115">**Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <span data-ttu-id="15987-116">При использовании поставщика OLE DB для Microsoft Jet, коллекции **представлений** метод **Append** позволит можно использовать для определения **процедуры** , а не в **представлении** с помощью параметра *командной* .</span><span class="sxs-lookup"><span data-stu-id="15987-116">When using the OLE DB Provider for Microsoft Jet, the **Views** collection **Append** method will allow you to specify a **Procedure** rather than a **View** in the *Command* parameter.</span></span> <span data-ttu-id="15987-117">**Процедуры** добавляются к источнику данных и добавляются в коллекцию **представлений** .</span><span class="sxs-lookup"><span data-stu-id="15987-117">The **Procedure** will be added to the data source and will be added to the **Views** collection.</span></span> <span data-ttu-id="15987-118">После **добавления**при обновлении семейств сайтов **процедуры** и **представления** **процедуры** больше не будет находиться в коллекции **представлений** и будет отображаться в коллекции **процедур** .</span><span class="sxs-lookup"><span data-stu-id="15987-118">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **Procedure** will no longer be in the **Views** collection and will appear in the **Procedures** collection.</span></span>


