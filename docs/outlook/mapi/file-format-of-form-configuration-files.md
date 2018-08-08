---
title: Формат файла из файлов конфигурации формы
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 86e4ebd9-6df2-4346-9ce9-580f80a83884
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: def91b4e28e60f6d2e8534f0ed7261777ec0c8e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808421"
---
# <a name="file-format-of-form-configuration-files"></a><span data-ttu-id="b102f-103">Формат файла из файлов конфигурации формы</span><span class="sxs-lookup"><span data-stu-id="b102f-103">File format of form configuration files</span></span>

<span data-ttu-id="b102f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b102f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b102f-105">Файл конфигурации формы представляет собой форматированный файл, созданных разработчиками форм для определения формы.</span><span class="sxs-lookup"><span data-stu-id="b102f-105">A form configuration file is a formatted file created by form developers to define a form.</span></span>
  
<span data-ttu-id="b102f-106">Так как файлы конфигурации форм используются руководителями формы для загрузки формы, каждая форма должна быть определена с помощью файла конфигурации формы.</span><span class="sxs-lookup"><span data-stu-id="b102f-106">Because form configuration files are used by form managers to load forms, each form must be defined using a form configuration file.</span></span> <span data-ttu-id="b102f-107">Файлы конфигурации форм должны иметь расширение имени файла .cfg.</span><span class="sxs-lookup"><span data-stu-id="b102f-107">Form configuration files must have the .cfg filename extension.</span></span> <span data-ttu-id="b102f-108">Файл следует общий синтаксис файла инициализации Windows (INI-файла).</span><span class="sxs-lookup"><span data-stu-id="b102f-108">The file follows the general syntax of a Windows initialization file (.ini file).</span></span> 

<span data-ttu-id="b102f-109">Он содержит именованные разделы, а каждый раздел содержит ряд записей и их значения.</span><span class="sxs-lookup"><span data-stu-id="b102f-109">It is divided into named sections, and each section contains a series of entries and values.</span></span> <span data-ttu-id="b102f-110">Значения использовать одну из следующих типов: string, отображается строка, строка платформы, путь, целое число или глобальный уникальный идентификатор **GUID**.</span><span class="sxs-lookup"><span data-stu-id="b102f-110">Values have one of the following types: string, displayed string, platform string, path, integer, or globally unique identifier, **GUID**.</span></span> <span data-ttu-id="b102f-111">Файлы конфигурации форм можно создать с помощью любого текстового редактора или текстового процессора, способный сохранении текстовых файлов.</span><span class="sxs-lookup"><span data-stu-id="b102f-111">Form configuration files can be created with any text editor or word processor that is capable of saving text files.</span></span>
  

