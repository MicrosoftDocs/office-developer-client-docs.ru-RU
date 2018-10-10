---
title: Append Method (ADOX Views)
TOCTitle: Append Method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 106dd9d72cb350422f00da05859bc096cb2b52e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481505"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="246e3-102">Append Method (ADOX Views)</span><span class="sxs-lookup"><span data-stu-id="246e3-102">Append Method (ADOX Views)</span></span>


<span data-ttu-id="246e3-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="246e3-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="246e3-104">Создает новый объект [представления](view-object-adox.md) и добавляет его в коллекцию [представлений](views-collection-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="246e3-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="246e3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="246e3-105">Syntax</span></span>

<span data-ttu-id="246e3-106">*Представления*. Добавьте*имя*, *команда*</span><span class="sxs-lookup"><span data-stu-id="246e3-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="246e3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="246e3-107">Parameters</span></span>

  - <span data-ttu-id="246e3-108">*Имя*</span><span class="sxs-lookup"><span data-stu-id="246e3-108">*Name*</span></span>

  - <span data-ttu-id="246e3-109">**Строковое** значение, задающее имя представления для создания.</span><span class="sxs-lookup"><span data-stu-id="246e3-109">A **String** value that specifies the name of the view to create.</span></span>

  - <span data-ttu-id="246e3-110">*Команда*</span><span class="sxs-lookup"><span data-stu-id="246e3-110">*Command*</span></span>

  - <span data-ttu-id="246e3-111">Объект ADO [команды](command-object-ado.md) , представляющий представление для создания.</span><span class="sxs-lookup"><span data-stu-id="246e3-111">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>

## <a name="remarks"></a><span data-ttu-id="246e3-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="246e3-112">Remarks</span></span>

<span data-ttu-id="246e3-113">Создает новое представление источника данных с именем и атрибуты, указанные в объекте **команды** .</span><span class="sxs-lookup"><span data-stu-id="246e3-113">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="246e3-114">Если текст команды, который пользователь вводит представляет процедуры, а не как представление, поведение зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="246e3-114">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider.</span></span> <span data-ttu-id="246e3-115">**Добавление** завершится ошибкой, если поставщик не поддерживает сохранение команды.</span><span class="sxs-lookup"><span data-stu-id="246e3-115">**Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <P><span data-ttu-id="246e3-116">При использовании поставщика OLE DB для Microsoft Jet, коллекции <STRONG>представлений</STRONG> метод <STRONG>Append</STRONG> позволит можно использовать для определения <STRONG>процедуры</STRONG> , а не в <STRONG>представлении</STRONG> с помощью параметра <EM>командной</EM> .</span><span class="sxs-lookup"><span data-stu-id="246e3-116">When using the OLE DB Provider for Microsoft Jet, the <STRONG>Views</STRONG> collection <STRONG>Append</STRONG> method will allow you to specify a <STRONG>Procedure</STRONG> rather than a <STRONG>View</STRONG> in the <EM>Command</EM> parameter.</span></span> <span data-ttu-id="246e3-117"><STRONG>Процедуры</STRONG> добавляются к источнику данных и добавляются в коллекцию <STRONG>представлений</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="246e3-117">The <STRONG>Procedure</STRONG> will be added to the data source and will be added to the <STRONG>Views</STRONG> collection.</span></span> <span data-ttu-id="246e3-118">После <STRONG>добавления</STRONG>при обновлении семейств сайтов <STRONG>процедуры</STRONG> и <STRONG>представления</STRONG> <STRONG>процедуры</STRONG> больше не будет находиться в коллекции <STRONG>представлений</STRONG> и будет отображаться в коллекции <STRONG>процедур</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="246e3-118">After the <STRONG>Append</STRONG>, if the <STRONG>Procedures</STRONG> and <STRONG>Views</STRONG> collections are refreshed, the <STRONG>Procedure</STRONG> will no longer be in the <STRONG>Views</STRONG> collection and will appear in the <STRONG>Procedures</STRONG> collection.</span></span></P>


