<template>
  <details class="dropdown dropdown-end">
    <summary class="btn btn-ghost rounded-md">
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
           class="size-6">
        <path stroke-linecap="round" stroke-linejoin="round"
              d="M12 6.75a.75.75 0 1 1 0-1.5.75.75 0 0 1 0 1.5ZM12 12.75a.75.75 0 1 1 0-1.5.75.75 0 0 1 0 1.5ZM12 18.75a.75.75 0 1 1 0-1.5.75.75 0 0 1 0 1.5Z"/>
      </svg>
    </summary>
    <ul class="menu dropdown-content bg-base-100 rounded-box z-1 w-52 p-2 shadow-sm">
      <li><a onclick="editModal.showModal()">Edit</a></li>
      <li><a onclick="deleteModal.showModal()">Delete</a></li>
    </ul>
  </details>

  <dialog id="editModal" class="modal">
    <div class="modal-box">
      <h3 class="text-lg font-bold">Edit Url</h3>
      <div>
        <form method="dialog">
          <fieldset class="fieldset space-y-2 w-full">
            <label class="label">Name</label>
            <input type="text" class="input w-full" placeholder="Name"/>
            <label class="label">Description</label>
            <textarea rows="2" class="textarea w-full" placeholder="Description"/>
            <label class="label">Url</label>
            <input type="text" class="input w-full" placeholder="Url"/>
            <button class="btn btn-neutral w-full" @click="updateUrl(props.urlId)">Update</button>
            <button class="btn w-full">Close</button>
          </fieldset>
        </form>
      </div>
    </div>
  </dialog>

  <dialog id="deleteModal" class="modal">
    <div class="modal-box">
      <h3 class="text-lg font-bold">Delete Url</h3>
      <p class="py-4">Are you sure you want to delete this url?</p>
      <div class="modal-action">
        <form method="dialog">
          <!-- if there is a button in form, it will close the modal -->
          <button class="btn btn-error" @click="deleteUrl(props.urlId)">Delete</button>
          <button class="btn">Close</button>
        </form>
      </div>
    </div>
  </dialog>
</template>

<script setup lang="ts">
const props = defineProps<{ urlId: string }>();

function updateUrl(id: string) {
  console.log(`updating url with id ${id}`);
}

function deleteUrl(id: string) {
  console.log(`deleting url with id ${id}`);
}
</script>