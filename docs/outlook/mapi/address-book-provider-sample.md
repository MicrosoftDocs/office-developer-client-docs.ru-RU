---
title: Пример поставщика адресной книги
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331110"
---
# <a name="address-book-provider-sample"></a><span data-ttu-id="d9a7e-103">Пример поставщика адресной книги</span><span class="sxs-lookup"><span data-stu-id="d9a7e-103">Address Book Provider Sample</span></span>

  
  
<span data-ttu-id="d9a7e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9a7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9a7e-105">В этом примере поддерживается один контейнер "только для чтения" для отображаемых имен и адресов электронной почты, которые считываются из плоского двоичного файла.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-105">This sample supports a single read-only container for display names and email addresses, which are read from a flat binary file.</span></span> <span data-ttu-id="d9a7e-106">В этом примере поддерживаются одноразовые шаблоны и все параметры конфигурации, кроме мастера профилей.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-106">The sample supports one-off templates and all configuration options except the Profile Wizard.</span></span>
  
<span data-ttu-id="d9a7e-107">Этот пример можно скачать из [примеров кода для API обмена сообщенияМи Outlook (MAPI)](https://go.microsoft.com/fwlink/?LinkId=129740
).</span><span class="sxs-lookup"><span data-stu-id="d9a7e-107">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740
).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d9a7e-108">Выполним</span><span class="sxs-lookup"><span data-stu-id="d9a7e-108">Executable:</span></span>  <br/> |<span data-ttu-id="d9a7e-109">SABP32. dll</span><span class="sxs-lookup"><span data-stu-id="d9a7e-109">SABP32.dll</span></span>  <br/> |
| <span data-ttu-id="d9a7e-110">Каталог исходного кода:</span><span class="sxs-lookup"><span data-stu-id="d9a7e-110">Source code directory:</span></span>  <br/> |<span data-ttu-id="d9a7e-111">Самплеаддрессбукпровидер\сабп</span><span class="sxs-lookup"><span data-stu-id="d9a7e-111">SampleAddressBookProvider\SABP</span></span>  <br/> |
|<span data-ttu-id="d9a7e-112">Языки</span><span class="sxs-lookup"><span data-stu-id="d9a7e-112">Language:</span></span>  <br/> |<span data-ttu-id="d9a7e-113">Языка</span><span class="sxs-lookup"><span data-stu-id="d9a7e-113">C++</span></span>  <br/> |
|<span data-ttu-id="d9a7e-114">Embedded</span><span class="sxs-lookup"><span data-stu-id="d9a7e-114">Platforms:</span></span>  <br/> |<span data-ttu-id="d9a7e-115">Microsoft Visual Studio 2008 для компиляции для Windows Vista, Windows Server 2008, Windows XP с ПАКЕТом обновления 2 (SP2) и Windows Server 2003 SP1</span><span class="sxs-lookup"><span data-stu-id="d9a7e-115">Microsoft Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="d9a7e-116">Поддерживаемые функции</span><span class="sxs-lookup"><span data-stu-id="d9a7e-116">Supported Features</span></span>

<span data-ttu-id="d9a7e-117">В этом примере поддерживаются следующие функции:</span><span class="sxs-lookup"><span data-stu-id="d9a7e-117">This sample supports the following features:</span></span>
  
- <span data-ttu-id="d9a7e-118">Ограничения для таблиц.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-118">Table restrictions.</span></span> <span data-ttu-id="d9a7e-119">В этом примере реализуется разрешение на сопоставление префиксов и неоднозначных имен.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-119">The sample implements prefix-match and ambiguous-name resolution.</span></span> <span data-ttu-id="d9a7e-120">Он не реализует полный язык ограничений MAPI, а ограничения поддерживаются только для отображаемого имени.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-120">It does not implement the full MAPI restriction language, and restrictions are supported only on the display name.</span></span>
    
- <span data-ttu-id="d9a7e-121">Таблица отображения сведений для пользователей обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-121">A details display table for messaging users.</span></span> 
    
- <span data-ttu-id="d9a7e-122">Один адрес.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-122">One-off addresses.</span></span>
    
- <span data-ttu-id="d9a7e-123">Диалоговое окно расширенного поиска.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-123">An advanced search dialog box.</span></span>
    
- <span data-ttu-id="d9a7e-124">Интерфейс [имапистатус: IMAPIProp](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="d9a7e-124">An [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="d9a7e-125">Этот интерфейс частично поддерживается; его методы **IMAPIProp** делегируются интерфейсу **ипропдата** .</span><span class="sxs-lookup"><span data-stu-id="d9a7e-125">This interface is partially supported; its **IMAPIProp** methods are delegated to the **IPropData** interface.</span></span> <span data-ttu-id="d9a7e-126">Дополнительные сведения см. в интерфейсе [ипропдата: IMAPIProp](ipropdataimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="d9a7e-126">For more information, see the [IPropData : IMAPIProp](ipropdataimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="d9a7e-127">Интерактивная и программная конфигурация.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-127">Interactive and programmatic configuration.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="d9a7e-128">Неподдерживаемые функции</span><span class="sxs-lookup"><span data-stu-id="d9a7e-128">Unsupported Features</span></span>

<span data-ttu-id="d9a7e-129">В этом примере не поддерживаются следующие функции:</span><span class="sxs-lookup"><span data-stu-id="d9a7e-129">This sample does not support the following features:</span></span>
  
- <span data-ttu-id="d9a7e-130">Порядок.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-130">Sorting.</span></span>
    
- <span data-ttu-id="d9a7e-131">Списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-131">Distribution lists.</span></span>
    
- <span data-ttu-id="d9a7e-132">Создание, удаление и изменение записей.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-132">Creating, deleting, and modifying entries.</span></span>
    
- <span data-ttu-id="d9a7e-133">Свойства с несколькими значениями.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-133">Properties with multiple values.</span></span>
    
- <span data-ttu-id="d9a7e-134">Именованные свойства.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-134">Named properties.</span></span>
    
- <span data-ttu-id="d9a7e-135">Различия между первым и последним именами в отображаемых именах;</span><span class="sxs-lookup"><span data-stu-id="d9a7e-135">Distinguishing between first and last names in display names.</span></span>
    
 <span data-ttu-id="d9a7e-136">**Установка образца поставщика адресных книг**</span><span class="sxs-lookup"><span data-stu-id="d9a7e-136">**To install the Sample Address Book Provider**</span></span>
  
1. <span data-ttu-id="d9a7e-137">Чтобы скачать образец поставщика адресных книг, ознакомьтесь [со статьЕй скачивание образцов Outlook MAPI](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="d9a7e-137">To download the Sample Address Book Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="d9a7e-138">Откройте папку, в которую были сохранены примеры Outlook MAPI.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-138">Locate the folder where you saved the Outlook MAPI Samples.</span></span> <span data-ttu-id="d9a7e-139">Щелкните правой кнопкой мыши папку Zip **\<аутлукмаписамплес-\> Version Number** и выберите **извлечь все**.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-139">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="d9a7e-140">Нажмите кнопку **Обзор**, выберите расположение, в котором нужно сохранить пример, и нажмите кнопку **извлечь**.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-140">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="d9a7e-141">Запустите Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-141">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="d9a7e-142">В Visual Studio 2008 откройте меню **файл**, выберите пункт **Открыть**, а затем выберите **проект/решение**.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-142">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="d9a7e-143">Перейдите к папке, в которой сохранен пример, выберите **САБП. vcproj**, а затем нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-143">Browse to the location where you saved the sample, click **SABP.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="d9a7e-144">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-144">On the **Build** menu, click **Build Solution**.</span></span>
    
8. <span data-ttu-id="d9a7e-145">В диалоговом окне **сохранить файл как** нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-145">In the **Save File As** dialog box, click **Save**.</span></span>
    
9. <span data-ttu-id="d9a7e-146">В папке, в которой сохранен пример, щелкните файл **install. bat** правой кнопкой мыши и выберите пункт **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-146">In the folder where you saved the sample, right-click the **install.bat** file and click **Run as administrator**.</span></span>
    
10. <span data-ttu-id="d9a7e-147">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-147">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="d9a7e-148">**Install. bat** копирует библиотеку DLL в папку установки Microsoft Office по умолчанию, C:\Program Files\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-148">**Install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="d9a7e-149">Если вы установили продукты Office в другом расположении, щелкните правой кнопкой мыши **install. bat** и выберите команду **изменить**.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-149">If you have installed Office products in a different location, right-click **Install.bat** and click **Edit**.</span></span> <span data-ttu-id="d9a7e-150">Файл откроется в блокноте.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-150">The file opens in Notepad.</span></span> <span data-ttu-id="d9a7e-151">Замените путь установки по умолчанию на путь установки, используемый на вашем компьютере.</span><span class="sxs-lookup"><span data-stu-id="d9a7e-151">Replace the default installation path with the installation path used on your computer.</span></span> 
  

