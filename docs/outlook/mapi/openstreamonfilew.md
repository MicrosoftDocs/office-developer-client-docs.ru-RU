---
title: OpenStreamOnFileW
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenStreamOnFileW
api_type:
- COM
ms.assetid: 263b9f24-eac8-4d34-8f66-dc87024b94b9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7e67d84320b57fe6e510b70a68088f289ef6030d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406026"
---
# <a name="openstreamonfilew"></a><span data-ttu-id="c3d6f-103">OpenStreamOnFileW</span><span class="sxs-lookup"><span data-stu-id="c3d6f-103">OpenStreamOnFileW</span></span>

  
  
<span data-ttu-id="c3d6f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3d6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3d6f-105">Выделяет и инициализирует объект OLE **IStream** для доступа к содержимому файла.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-105">Allocates and initializes an OLE **IStream** object to access the contents of a file.</span></span> <span data-ttu-id="c3d6f-106">Эта функция принимает строки в КОДИРОВКе Юникод в качестве аргументов, в отличие от ANSI версии этой функции [опенстреамонфиле](openstreamonfile.md), и таким образом позволяет использовать в имени файла произвольные символы, включая путь и расширение файла.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-106">This function takes UNICODE strings as arguments, unlike the ANSI version of this function [OpenStreamOnFile](openstreamonfile.md), and thus allows for arbitrary characters in the file name including the path and file extension.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c3d6f-107">Экспортировано:</span><span class="sxs-lookup"><span data-stu-id="c3d6f-107">Exported by:</span></span>  <br/> |<span data-ttu-id="c3d6f-108">olmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="c3d6f-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="c3d6f-109">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="c3d6f-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="c3d6f-110">Outlook</span><span class="sxs-lookup"><span data-stu-id="c3d6f-110">Outlook</span></span>  <br/> |
|<span data-ttu-id="c3d6f-111">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="c3d6f-111">Called by:</span></span>  <br/> |<span data-ttu-id="c3d6f-112">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="c3d6f-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT STDMETHODCALLTYPE OpenStreamOnFileW(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  LPWSTR lpszFileName,
  LPWSTR lpszPrefix,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="c3d6f-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3d6f-113">Parameters</span></span>

 <span data-ttu-id="c3d6f-114">_Лпаллокатебуффер_</span><span class="sxs-lookup"><span data-stu-id="c3d6f-114">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="c3d6f-115">возврата Указатель на функцию [мапиаллокатебуффер](mapiallocatebuffer.md) , которая будет использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-115">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="c3d6f-116">_Лпфрибуффер_</span><span class="sxs-lookup"><span data-stu-id="c3d6f-116">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="c3d6f-117">возврата Указатель на функцию [мапифрибуффер](mapifreebuffer.md) , который будет использоваться для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-117">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="c3d6f-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c3d6f-118">_ulFlags_</span></span>
  
> <span data-ttu-id="c3d6f-119">возврата Битовая маска флагов, используемых для управления созданием или открытием файла, к которому можно получить доступ через объект OLE **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c3d6f-119">[in] Bitmask of flags used to control the creation or opening of the file to be accessed through the OLE **IStream** object.</span></span> <span data-ttu-id="c3d6f-120">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="c3d6f-120">The following flags can be set:</span></span> 
    
<span data-ttu-id="c3d6f-121">СОФ_УНИКУЕФИЛЕНАМЕ</span><span class="sxs-lookup"><span data-stu-id="c3d6f-121">SOF_UNIQUEFILENAME</span></span>
  
> <span data-ttu-id="c3d6f-122">Для объекта **IStream** будет создан временный файл.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-122">A temporary file is to be created for the **IStream** object.</span></span> <span data-ttu-id="c3d6f-123">Если этот флаг установлен, также должны быть заданы флаги СТГМ_КРЕАТЕ и СТГМ_РЕАДВРИТЕ.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-123">If this flag is set, the STGM_CREATE and STGM_READWRITE flags should also be set.</span></span> 
    
<span data-ttu-id="c3d6f-124">СТГМ_КРЕАТЕ</span><span class="sxs-lookup"><span data-stu-id="c3d6f-124">STGM_CREATE</span></span>
  
> <span data-ttu-id="c3d6f-125">Файл будет создан, даже если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-125">The file is to be created even if one already exists.</span></span> <span data-ttu-id="c3d6f-126">Если параметр _лпсзфиленаме_ не задан, то этот флаг и стгм_делетеонрелеасе должны быть установлены.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-126">If the  _lpszFileName_ parameter is not set, both this flag and STGM_DELETEONRELEASE must be set.</span></span> <span data-ttu-id="c3d6f-127">Если задано значение СТГМ_КРЕАТЕ, то флаг СТГМ_РЕАДВРИТЕ также должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-127">If STGM_CREATE is set, the STGM_READWRITE flag must also be set.</span></span> 
    
<span data-ttu-id="c3d6f-128">СТГМ_ДЕЛЕТЕОНРЕЛЕАСЕ</span><span class="sxs-lookup"><span data-stu-id="c3d6f-128">STGM_DELETEONRELEASE</span></span>
  
> <span data-ttu-id="c3d6f-129">Файл будет удален при отпускании объекта **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c3d6f-129">The file is to be deleted when the **IStream** object is released.</span></span> <span data-ttu-id="c3d6f-130">Если параметр _лпсзфиленаме_ не задан, то этот флаг и стгм_креате должны быть установлены.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-130">If the  _lpszFileName_ parameter is not set, both this flag and STGM_CREATE must be set.</span></span> 
    
<span data-ttu-id="c3d6f-131">СТГМ_РЕАД</span><span class="sxs-lookup"><span data-stu-id="c3d6f-131">STGM_READ</span></span>
  
> <span data-ttu-id="c3d6f-132">Файл будет создан или открыт с доступом только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-132">The file is to be created or opened with read-only access.</span></span>
    
<span data-ttu-id="c3d6f-133">СТГМ_РЕАДВРИТЕ</span><span class="sxs-lookup"><span data-stu-id="c3d6f-133">STGM_READWRITE</span></span>
  
> <span data-ttu-id="c3d6f-134">Файл будет создан или открыт с разрешением на чтение и запись.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-134">The file is to be created or opened with read/write permission.</span></span> <span data-ttu-id="c3d6f-135">Если этот флаг не установлен, то флаг СТГМ_КРЕАТЕ не должен быть установлен или.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-135">If this flag is not set, the STGM_CREATE flag must not be set either.</span></span>
    
 <span data-ttu-id="c3d6f-136">_Лпсзфиленаме_</span><span class="sxs-lookup"><span data-stu-id="c3d6f-136">_lpszFileName_</span></span>
  
> <span data-ttu-id="c3d6f-137">возврата Имя файла, включая путь и расширение, имени файла в Юникоде, для которого **опенстреамонфилев** Инициализирует объект **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c3d6f-137">[in] The filename, including path and extension, of the Unicode named file for which **OpenStreamOnFileW** initializes the **IStream** object.</span></span> <span data-ttu-id="c3d6f-138">Если установлен флаг СОФ_УНИКУЕФИЛЕНАМЕ, _лпсзфиленаме_ содержит путь к каталогу, в котором необходимо создать временный файл.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-138">If the SOF_UNIQUEFILENAME flag is set,  _lpszFileName_ contains the path to the directory in which to create a temporary file.</span></span> <span data-ttu-id="c3d6f-139">Если _лпсзфиленаме_ имеет значение null, **опенстреамонфилев** получает соответствующий путь от системы, и оба флага стгм_креате и стгм_делетеонрелеасе должны быть установлены.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-139">If  _lpszFileName_ is NULL, **OpenStreamOnFileW** obtains an appropriate path from the system, and both the STGM_CREATE and STGM_DELETEONRELEASE flags must be set.</span></span> 
    
 <span data-ttu-id="c3d6f-140">_Лпсзпрефикс_</span><span class="sxs-lookup"><span data-stu-id="c3d6f-140">_lpszPrefix_</span></span>
  
> <span data-ttu-id="c3d6f-141">возврата Префикс имени файла Юникод, в котором **опенстреамонфилев** Инициализирует объект **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c3d6f-141">[in] The prefix for the Unicode filename on which **OpenStreamOnFileW** initializes the **IStream** object.</span></span> <span data-ttu-id="c3d6f-142">Если этот параметр установлен, префикс должен содержать не более трех символов.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-142">If set, the prefix must contain not more than three characters.</span></span> <span data-ttu-id="c3d6f-143">Если _лпсзпрефикс_ имеет значение null, используется префикс "SOF".</span><span class="sxs-lookup"><span data-stu-id="c3d6f-143">If  _lpszPrefix_ is NULL, a prefix of "SOF" is used.</span></span> 
    
 <span data-ttu-id="c3d6f-144">_Лппстреам_</span><span class="sxs-lookup"><span data-stu-id="c3d6f-144">_lppStream_</span></span>
  
> <span data-ttu-id="c3d6f-145">вышли Указатель на указатель на объект, который предоставляет интерфейс **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c3d6f-145">[out] Pointer to a pointer to an object exposing the **IStream** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c3d6f-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3d6f-146">Return value</span></span>

<span data-ttu-id="c3d6f-147">S_OK</span><span class="sxs-lookup"><span data-stu-id="c3d6f-147">S_OK</span></span>
  
> <span data-ttu-id="c3d6f-148">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-148">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c3d6f-149">МАПИ_Е_НО_АКЦЕСС</span><span class="sxs-lookup"><span data-stu-id="c3d6f-149">MAPI_E_NO_ACCESS</span></span>
  
> <span data-ttu-id="c3d6f-150">Доступ к файлу невозможен из-за недостаточного разрешения пользователя или изменения файлов, доступных только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-150">The file could not be accessed due to insufficient user permissions or because read-only files cannot be modified.</span></span>
    
<span data-ttu-id="c3d6f-151">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="c3d6f-151">MAPI_E_NOT_FOUND</span></span>
  
> <span data-ttu-id="c3d6f-152">Указанный файл не существует.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-152">The designated file does not exist.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c3d6f-153">Примечания</span><span class="sxs-lookup"><span data-stu-id="c3d6f-153">Remarks</span></span>

<span data-ttu-id="c3d6f-154">Функция **опенстреамонфилев** имеет два важных применения в дополнение к обработке файла с именем в Юникоде, в отличие от параметра флага соф_уникуефиленаме.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-154">The **OpenStreamOnFileW** function has two important uses in addition to handling a file with a Unicode name, distinguished by the setting of the SOF_UNIQUEFILENAME flag.</span></span> <span data-ttu-id="c3d6f-155">Если этот флаг не задан, **опенстреамонфилев** открывает объект **IStream** для существующего файла, например для копирования его содержимого в свойство **пр_аттач_дата_бин** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) вложения с помощью \*\* IStream:: метод CopyTo\*\* .</span><span class="sxs-lookup"><span data-stu-id="c3d6f-155">When this flag is not set, **OpenStreamOnFileW** opens an **IStream** object on an existing file, for example to copy its contents to the **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) property of an attachment using the **IStream::CopyTo** method.</span></span> <span data-ttu-id="c3d6f-156">В этом случае параметр _лпсзфиленаме_ указывает путь и имя файла.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-156">In this case the  _lpszFileName_ parameter specifies the path and filename of the file.</span></span> 
  
<span data-ttu-id="c3d6f-157">Если задано значение СОФ_УНИКУЕФИЛЕНАМЕ, **опенстреамонфилев** создает временный файл для хранения данных для объекта **IStream** .</span><span class="sxs-lookup"><span data-stu-id="c3d6f-157">When SOF_UNIQUEFILENAME is set, **OpenStreamOnFileW** creates a temporary file to hold data for an **IStream** object.</span></span> <span data-ttu-id="c3d6f-158">В этом случае параметр _лпсзфиленаме_ может указать путь к каталогу, в котором будет создан файл, а параметр _лпсзпрефикс_ можно указать префикс для имени файла.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-158">For this usage, the  _lpszFileName_ parameter can optionally designate the path to the directory where the file is to be created, and the  _lpszPrefix_ parameter can optionally specify a prefix for the filename.</span></span> 
  
<span data-ttu-id="c3d6f-159">Когда вызывающий клиентское приложение или поставщик услуг завершает работу с объектом **IStream** , он должен освободить его, вызвав метод OLE **IStream:: Release** .</span><span class="sxs-lookup"><span data-stu-id="c3d6f-159">When the calling client application or service provider is finished with the **IStream** object, it should free it by calling the OLE **IStream::Release** method.</span></span> 
  
<span data-ttu-id="c3d6f-160">MAPI использует функции, на которые указывает _лпаллокатебуффер_ и _лпфрибуффер_ для большей части памяти и освобождений, в частности, для выделения памяти, используемой клиентскими приложениями при вызове интерфейсов объектов, таких как [IMAPIProp:: Props](imapiprop-getprops.md) и [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="c3d6f-160">MAPI uses the functions pointed to by  _lpAllocateBuffer_ and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c3d6f-161">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="c3d6f-161">Notes to callers</span></span>

<span data-ttu-id="c3d6f-162">Флаг СОФ_УНИКУЕФИЛЕНАМЕ используется для создания временного файла с именем, уникальным для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-162">The SOF_UNIQUEFILENAME flag is used to create a temporary file with a name unique to the messaging system.</span></span> <span data-ttu-id="c3d6f-163">Если этот флаг установлен, параметр _лпсзфиленаме_ спеЦифес путь к временному файлу, а параметр _лпсзпрефикс_ содержит префиксные символы имени файла.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-163">If this flag is set, the  _lpszFileName_ parameter specifes the path for the temporary file, and the  _lpszPrefix_ parameter contains the prefix characters of the filename.</span></span> <span data-ttu-id="c3d6f-164">Сконструированное имя файла <prefix>— hhhh. TMP, где HHHH — это шестнадцатеричное число.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-164">The constructed filename is <prefix>HHHH.TMP, where HHHH is a hexadecimal number.</span></span> <span data-ttu-id="c3d6f-165">Если _лпсзфиленаме_ имеет значение null, файл будет создан во временном каталоге файлов, который возвращается из функции Windows **жеттемппас**, или из текущего каталога, если не указан временный каталог файлов.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-165">If  _lpszFileName_ is NULL, the file will be created in the temporary file directory that is returned from the Windows function **GetTempPath**, or the current directory if no temporary file directory has been designated.</span></span>
  
<span data-ttu-id="c3d6f-166">Если флаг СОФ_УНИКУЕФИЛЕНАМЕ не установлен, то _лпсзпрефикс_ игнорируется, а _лпсзфиленаме_ должен содержать полный путь и имя файла, который требуется открыть или создать.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-166">If the SOF_UNIQUEFILENAME flag is not set,  _lpszPrefix_ is ignored, and  _lpszFileName_ should contain the fully qualified path and filename of the file to be opened or created.</span></span> <span data-ttu-id="c3d6f-167">Файл будет открыт или создан на основе других флагов, заданных в _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="c3d6f-167">The file will be opened or created based on the other flags that are set in  _ulFlags_.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c3d6f-168">См. также</span><span class="sxs-lookup"><span data-stu-id="c3d6f-168">See also</span></span>



[<span data-ttu-id="c3d6f-169">OpenStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="c3d6f-169">OpenStreamOnFile</span></span>](openstreamonfile.md)

