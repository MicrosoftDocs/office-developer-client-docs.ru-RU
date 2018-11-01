---
title: Действия OpenDiagram макроса
TOCTitle: OpenDiagram Macro Action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3118c2a6b85d400b4b797c4b9b711e5f5a512c62
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869241"
---
# <a name="opendiagram-macro-action"></a><span data-ttu-id="decc2-102">Действия OpenDiagram макроса</span><span class="sxs-lookup"><span data-stu-id="decc2-102">OpenDiagram Macro Action</span></span>


<span data-ttu-id="decc2-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="decc2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="decc2-104">В проекте Microsoft Access можно использовать действие **OpenDiagram** для открытия схемы базы данных в режиме конструктора.</span><span class="sxs-lookup"><span data-stu-id="decc2-104">In an Access project, you can use the **OpenDiagram** action to open a database diagram in Design view.</span></span>


> [!NOTE]
> <P><span data-ttu-id="decc2-p101">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="decc2-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="decc2-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="decc2-107">Setting</span></span>

<span data-ttu-id="decc2-108">Действие **OpenDiagram** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="decc2-108">The **OpenDiagram** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="decc2-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="decc2-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="decc2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="decc2-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="decc2-111"><strong>Имя схемы</strong></span><span class="sxs-lookup"><span data-stu-id="decc2-111"><strong>Diagram Name</strong></span></span></p></td>
<td><p><span data-ttu-id="decc2-112">Имя схемы базы данных, чтобы открыть.</span><span class="sxs-lookup"><span data-stu-id="decc2-112">The name of the database diagram to open.</span></span> <span data-ttu-id="decc2-113">В поле <strong>Имя схемы</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов показывает все схемы базы данных в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="decc2-113">The <strong>Diagram Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all database diagrams in the current database.</span></span> <span data-ttu-id="decc2-114">Обязательный аргумент.</span><span class="sxs-lookup"><span data-stu-id="decc2-114">This is a required argument.</span></span> <span data-ttu-id="decc2-115">Если макрос, содержащий <strong>OpenDiagram</strong> действие в базе данных библиотеки, Microsoft Access сначала выполняет поиск схемы с этим именем в базе данных библиотеки, а затем в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="decc2-115">If you run a macro containing the <strong>OpenDiagram</strong> action in a library database, Microsoft Access first looks for the diagram with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="decc2-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="decc2-116">Remarks</span></span>

<span data-ttu-id="decc2-117">Это действие аналогично дважды щелкнув схемы базы данных в области навигации или щелкнув правой кнопкой мыши на схеме базы данных в области навигации и затем выбрав **Представление конструирования**.</span><span class="sxs-lookup"><span data-stu-id="decc2-117">This action is similar to double-clicking a database diagram in the Navigation Pane, or right-clicking the database diagram in the Navigation Pane and then clicking **Design View**.</span></span>


> [!TIP]
> <P><span data-ttu-id="decc2-118">Схемы базы данных можно перетаскивать из области переходов в строку действие в макросе.</span><span class="sxs-lookup"><span data-stu-id="decc2-118">You can drag a database diagram from the Navigation Pane to a macro action row.</span></span> <span data-ttu-id="decc2-119">Это автоматически создает <STRONG>ОткрытьСхему открывает схему базы данных в режиме конструктора</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="decc2-119">This automatically creates an <STRONG>OpenDiagram</STRONG> action that opens the database diagram in Design view.</span></span></P>



<span data-ttu-id="decc2-120">Чтобы выполнить действие **OpenDiagram** в Visual Basic для приложений (VBA) модуль, используйте метод **OpenDiagram** **объекта** .</span><span class="sxs-lookup"><span data-stu-id="decc2-120">To run the **OpenDiagram** action in a Visual Basic for Applications (VBA) module, use the **OpenDiagram** method of the **DoCmd** object.</span></span>

