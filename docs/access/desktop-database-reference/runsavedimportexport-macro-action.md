---
title: Макрокоманда RunSavedImportExport
TOCTitle: RunSavedImportExport macro action
ms:assetid: b2449c51-ee20-6e50-87f3-a45adc0b0dde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822018(v=office.15)
ms:contentKeyID: 48547165
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3022
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: adcc8a2a9462509f4b37d2dbdaf824387ae52a26
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309177"
---
# <a name="runsavedimportexport-macro-action"></a><span data-ttu-id="bc2d0-102">Макрокоманда RunSavedImportExport</span><span class="sxs-lookup"><span data-stu-id="bc2d0-102">RunSavedImportExport macro action</span></span>

<span data-ttu-id="bc2d0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc2d0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bc2d0-104">Вы можете использовать действие **рунсаведимпортекспорт** для запуска сохраненной спецификации импорта или экспорта, созданной с помощью мастера импорта или мастера экспорта.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-104">You can use the **RunSavedImportExport** action to run a saved import or export specification that you created by using the Import Wizard or the Export Wizard.</span></span>

> [!NOTE]
> <span data-ttu-id="bc2d0-105">Эта макрокоманда доступна только для доверенных баз данных.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-105">This action will not be allowed if the database is not trusted.</span></span>

## <a name="setting"></a><span data-ttu-id="bc2d0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc2d0-106">Setting</span></span>

<span data-ttu-id="bc2d0-107">Действие **рунсаведимпортекспорт** имеет следующий аргумент.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-107">The **RunSavedImportExport** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bc2d0-108">Аргумент макрокоманды</span><span class="sxs-lookup"><span data-stu-id="bc2d0-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="bc2d0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="bc2d0-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc2d0-110"><strong>Имя сохраненного экспортируемого импорта</strong></span><span class="sxs-lookup"><span data-stu-id="bc2d0-110"><strong>Saved Import Export Name</strong></span></span></p></td>
<td><p><span data-ttu-id="bc2d0-111">Выберите имя сохраненной спецификации импорта или экспорта из раскрывающегося списка.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-111">Select the name of a saved import or export specification from the drop-down list.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="bc2d0-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="bc2d0-112">Remarks</span></span>

- <span data-ttu-id="bc2d0-113">Эта макрокоманда имеет тот же результат, что и выполнение следующей процедуры в Access:</span><span class="sxs-lookup"><span data-stu-id="bc2d0-113">This macro action has the same effect as performing the following procedure in Access:</span></span>
    
  1.  <span data-ttu-id="bc2d0-114">На вкладке **Внешние данные** щелкните **Сохраненные операции импорта** или **Сохраненные экспорты**.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-114">On the **External Data** tab, click either **Saved Imports** or **Saved Exports**.</span></span>
    
  2.  <span data-ttu-id="bc2d0-115">В диалоговом окне **Управление задачами с данными** на вкладке Сохраненные операции **импорта** или **сохранения** (в зависимости от того, что выбрано на предыдущем шаге) выберите нужную спецификацию.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-115">In the **Manage Data Tasks** dialog box, on the **Saved Imports** or **Saved Exports** tab (depending on your choice in the preceding step), click the specification that you want to run.</span></span>
    
  3.  <span data-ttu-id="bc2d0-116">Нажмите кнопку **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-116">Click **Run**.</span></span>

- <span data-ttu-id="bc2d0-117">Перед выполнением действия **рунсаведимпортекспорт** убедитесь, что исходный и конечный файлы существуют, что исходные данные готовы для импорта и что операция случайно не перезапишет данные в конечном файле.</span><span class="sxs-lookup"><span data-stu-id="bc2d0-117">Before running the **RunSavedImportExport** action, make sure that the source and destination files exist, the source data is ready for importing, and that the operation will not accidentally overwrite any data in your destination file.</span></span>

- <span data-ttu-id="bc2d0-118">Ссылки на дополнительные сведения о сохранении и выполнении спецификаций импорта и экспорта можно найти в разделе " **см** .</span><span class="sxs-lookup"><span data-stu-id="bc2d0-118">Find links to more information about saving and running import and export specifications in the **See Also** section.</span></span>

- <span data-ttu-id="bc2d0-119">Если сохраненная спецификация импорта или экспорта, выбранная для сохраненного аргумента **имени импортируемОго импорта** , удаляется после создания макроса, при запуске макроса в Access отображается следующее сообщение об ошибке: **Спецификация с указанным индексом не существует. Укажите другой индекс. \* \* \* \* \* Имя спецификации \* \* \* \* \* '.**</span><span class="sxs-lookup"><span data-stu-id="bc2d0-119">If the saved import or export specification you choose for the **Saved Import Export Name** argument is deleted after the macro is created, Access displays the following error message when the macro is run: **The specification with the specified index does not exist. Specify a different index. '\*\*\*\*\*specification name\*\*\*\*\*'.**</span></span>

