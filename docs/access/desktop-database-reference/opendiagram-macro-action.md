---
title: Макрокоманда OpenDiagram
TOCTitle: OpenDiagram macro action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b04870a416874e2136e21b40c62d8e64a6182efe
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998548"
---
# <a name="opendiagram-macro-action"></a><span data-ttu-id="f82de-102">Макрокоманда OpenDiagram</span><span class="sxs-lookup"><span data-stu-id="f82de-102">OpenDiagram macro action</span></span>

<span data-ttu-id="f82de-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f82de-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f82de-104">В проекте Microsoft Access можно использовать действие **OpenDiagram** для открытия схемы базы данных в режиме конструктора.</span><span class="sxs-lookup"><span data-stu-id="f82de-104">In an Access project, you can use the **OpenDiagram** action to open a database diagram in Design view.</span></span>

> [!NOTE]
> <span data-ttu-id="f82de-105">Это действие не разрешено, если база данных не является доверенной.</span><span class="sxs-lookup"><span data-stu-id="f82de-105">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="f82de-106">Параметр</span><span class="sxs-lookup"><span data-stu-id="f82de-106">Setting</span></span>

<span data-ttu-id="f82de-107">Действие **OpenDiagram** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="f82de-107">The **OpenDiagram** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f82de-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="f82de-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="f82de-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f82de-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f82de-110"><strong>Имя схемы</strong></span><span class="sxs-lookup"><span data-stu-id="f82de-110"><strong>Diagram Name</strong></span></span></p></td>
<td><p><span data-ttu-id="f82de-111">Имя схемы базы данных, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="f82de-111">The name of the database diagram to open.</span></span> <span data-ttu-id="f82de-112">В поле <strong>Имя схемы</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов показывает все схемы базы данных в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="f82de-112">The <strong>Diagram Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all database diagrams in the current database.</span></span> <span data-ttu-id="f82de-113">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="f82de-113">This is a required argument.</span></span> <span data-ttu-id="f82de-114">Если макрос, содержащий <strong>OpenDiagram</strong> действие в базе данных библиотеки, Microsoft Access сначала выполняет поиск схемы с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="f82de-114">If you run a macro containing the <strong>OpenDiagram</strong> action in a library database, Microsoft Access first looks for the diagram with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a><span data-ttu-id="f82de-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="f82de-115">Remarks</span></span>

<span data-ttu-id="f82de-116">Это действие аналогично дважды щелкнув схемы базы данных в области навигации или щелкнув правой кнопкой мыши на схеме базы данных в области навигации и затем выбрав **Представление конструирования**.</span><span class="sxs-lookup"><span data-stu-id="f82de-116">This action is similar to double-clicking a database diagram in the Navigation Pane, or right-clicking the database diagram in the Navigation Pane and then clicking **Design View**.</span></span>

> [!TIP]
> <span data-ttu-id="f82de-117">Схемы базы данных можно перетаскивать из области переходов в строку действие в макросе.</span><span class="sxs-lookup"><span data-stu-id="f82de-117">You can drag a database diagram from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="f82de-118">Это автоматически создает **ОткрытьСхему открывает схему базы данных в режиме конструктора** .</span><span class="sxs-lookup"><span data-stu-id="f82de-118">This automatically creates an **OpenDiagram** action that opens the database diagram in Design view.</span></span>

<span data-ttu-id="f82de-119">Чтобы выполнить действие **OpenDiagram** в Visual Basic для приложений (VBA) модуль, используйте метод **OpenDiagram** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="f82de-119">To run the **OpenDiagram** action in a Visual Basic for Applications (VBA) module, use the **OpenDiagram** method of the **DoCmd** object.</span></span>

