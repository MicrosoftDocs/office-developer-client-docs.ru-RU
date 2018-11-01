---
title: Действия макроса RunSavedImportExport
TOCTitle: RunSavedImportExport Macro Action
ms:assetid: b2449c51-ee20-6e50-87f3-a45adc0b0dde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822018(v=office.15)
ms:contentKeyID: 48547165
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3022
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 48e808fa27e468dd7cb651cb5784627d5064fea0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870935"
---
# <a name="runsavedimportexport-macro-action"></a><span data-ttu-id="c4d5e-102">Действия макроса RunSavedImportExport</span><span class="sxs-lookup"><span data-stu-id="c4d5e-102">RunSavedImportExport Macro Action</span></span>


<span data-ttu-id="c4d5e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4d5e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c4d5e-104">Действие **RunSavedImportExport** можно использовать для запуска сохраненного импорта или экспорта спецификации, в которой была создана с помощью мастера импорта или мастер экспорта.</span><span class="sxs-lookup"><span data-stu-id="c4d5e-104">You can use the **RunSavedImportExport** action to run a saved import or export specification that you created by using the Import Wizard or the Export Wizard.</span></span>


> [!NOTE]
> <P><span data-ttu-id="c4d5e-p101">
		Эта действие не разрешено, если база данных не является доверенной. Дополнительные сведения о включении макросов см. по ссылкам в разделе See Also этой статьи.
</span><span class="sxs-lookup"><span data-stu-id="c4d5e-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="c4d5e-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="c4d5e-107">Setting</span></span>

<span data-ttu-id="c4d5e-108">Действие **RunSavedImportExport** использует следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="c4d5e-108">The **RunSavedImportExport** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c4d5e-109">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="c4d5e-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="c4d5e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="c4d5e-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4d5e-111"><strong>Имя сохраненной операции импорта экспорта</strong></span><span class="sxs-lookup"><span data-stu-id="c4d5e-111"><strong>Saved Import Export Name</strong></span></span></p></td>
<td><p><span data-ttu-id="c4d5e-112">Выберите имя сохраненного импорта или экспорта спецификации из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="c4d5e-112">Select the name of a saved import or export specification from the drop-down list.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c4d5e-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="c4d5e-113">Remarks</span></span>

  - <span data-ttu-id="c4d5e-114">Это действие макроса имеет тот же эффект, как в клиенте для выполнения следующей процедуры:</span><span class="sxs-lookup"><span data-stu-id="c4d5e-114">This macro action has the same effect as performing the following procedure in Access:</span></span>
    
    1.  <span data-ttu-id="c4d5e-115">На вкладке **Внешние данные** нажмите кнопку **Сохранения Imports** или **Сохранения экспорта**.</span><span class="sxs-lookup"><span data-stu-id="c4d5e-115">On the **External Data** tab, click either **Saved Imports** or **Saved Exports**.</span></span>
    
    2.  <span data-ttu-id="c4d5e-116">В диалоговом окне **Задачи управления данными** на вкладке **Сохранен Imports** или **Сохранения экспорта** (в зависимости от выбранного на предыдущем шаге), щелкните Спецификация, которую требуется запустить.</span><span class="sxs-lookup"><span data-stu-id="c4d5e-116">In the **Manage Data Tasks** dialog box, on the **Saved Imports** or **Saved Exports** tab (depending on your choice in the preceding step), click the specification that you want to run.</span></span>
    
    3.  <span data-ttu-id="c4d5e-117">Нажмите кнопку **выполнить**.</span><span class="sxs-lookup"><span data-stu-id="c4d5e-117">Click **Run**.</span></span>

  - <span data-ttu-id="c4d5e-118">Перед запуском **RunSavedImportExport** действие, убедитесь в том, что существует исходном и целевом файлы исходных данных готова для импорта и, что операция будет не удается перезаписать случайно все данные в файле назначения.</span><span class="sxs-lookup"><span data-stu-id="c4d5e-118">Before running the **RunSavedImportExport** action, make sure that the source and destination files exist, the source data is ready for importing, and that the operation will not accidentally overwrite any data in your destination file.</span></span>

  - <span data-ttu-id="c4d5e-119">Найдите ссылки на более подробные сведения о сохранении и выполнение импорта и экспорта спецификациями, указанными в разделе **См** .</span><span class="sxs-lookup"><span data-stu-id="c4d5e-119">Find links to more information about saving and running import and export specifications in the **See Also** section.</span></span>

  - <span data-ttu-id="c4d5e-120">Если сохраненного спецификации импорта или экспорта выберите для аргумента **Сохранения имени Импорт экспорт** удаляется после создания макрос, Access отображается следующее сообщение об ошибке при запуске макрос: спецификация с указанным индексом \*\* не существует. Укажите другой индекс. "\*\*\* Спецификация имя \***'.**</span><span class="sxs-lookup"><span data-stu-id="c4d5e-120">If the saved import or export specification you choose for the **Saved Import Export Name** argument is deleted after the macro is created, Access displays the following error message when the macro is run: **The specification with the specified index does not exist. Specify a different index. '\*\*\*\*\*specification name\*\*\*\*\*'.**</span></span>

