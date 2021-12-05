<template>
  <div>
    <!-- This example requires Tailwind CSS v2.0+ -->
    <div class="relative inline-block text-left">
      <div>
        <button
          type="button"
          class="inline-flex justify-center w-full rounded-md border border-gray-300 shadow-sm px-4 py-2 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-gray-100 focus:ring-indigo-500"
          id="menu-button"
          aria-expanded="true"
          aria-haspopup="true"
          @click="onCraftsDropDownClick"
        >
          Crafts Data
          <!-- Heroicon name: solid/chevron-down -->
          <svg
            class="-mr-1 ml-2 h-5 w-5"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
            fill="currentColor"
            aria-hidden="true"
          >
            <path
              fill-rule="evenodd"
              d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
              clip-rule="evenodd"
            />
          </svg>
        </button>
      </div>

      <!--
    Dropdown menu, show/hide based on menu state.

    Entering: "transition ease-out duration-100"
      From: "transform opacity-0 scale-95"
      To: "transform opacity-100 scale-100"
    Leaving: "transition ease-in duration-75"
      From: "transform opacity-100 scale-100"
      To: "transform opacity-0 scale-95"
  -->
      <div
        class="scale-95 origin-top-right absolute right-0 mt-2 w-56 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5 focus:outline-none"
        v-bind:class="
          isCraftsDropdownOpen
            ? 'transform opacity-100 scale-100'
            : 'transform opacity-0 scale-95 hidden'
        "
        role="menu"
        aria-orientation="vertical"
        aria-labelledby="menu-button"
        tabindex="-1"
      >
        <div class="py-1" role="none">
          <!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
          <a
            v-for="craft in craftsData"
            :key="craft.Id"
            @click="onCraftsItemClick"
            :data-craft-item-name="craft.Name"
            class="text-gray-700 block px-4 py-2 text-sm"
            role="menuitem"
            tabindex="-1"
            id="menu-item-0"
          >
            {{ craft.Name }}
          </a>
        </div>
      </div>
    </div>

        <div class="relative inline-block text-left">
      <div>
        <button
          type="button"
          class="inline-flex justify-center w-full rounded-md border border-gray-300 shadow-sm px-4 py-2 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-gray-100 focus:ring-indigo-500"
          id="menu-button"
          aria-expanded="true"
          aria-haspopup="true"
          @click="onObjectsDropDownClick"
        >
          Objects Data
          <!-- Heroicon name: solid/chevron-down -->
          <svg
            class="-mr-1 ml-2 h-5 w-5"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
            fill="currentColor"
            aria-hidden="true"
          >
            <path
              fill-rule="evenodd"
              d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
              clip-rule="evenodd"
            />
          </svg>
        </button>
      </div>

      <!--
    Dropdown menu, show/hide based on menu state.

    Entering: "transition ease-out duration-100"
      From: "transform opacity-0 scale-95"
      To: "transform opacity-100 scale-100"
    Leaving: "transition ease-in duration-75"
      From: "transform opacity-100 scale-100"
      To: "transform opacity-0 scale-95"
  -->
      <div
        class="scale-95 origin-top-right absolute right-0 mt-2 w-56 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5 focus:outline-none"
        v-bind:class="
          isObjectsDropdownOpen
            ? 'transform opacity-100 scale-100'
            : 'transform opacity-0 scale-95 hidden'
        "
        role="menu"
        aria-orientation="vertical"
        aria-labelledby="menu-button"
        tabindex="-1"
      >
        <div class="py-1" role="none">
          <!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
          <a
            v-for="object in objectsData"
            :key="object.Id"
            @click="onObjectsItemClick"
            :data-objects-item-name="object.Name"
            class="text-gray-700 block px-4 py-2 text-sm"
            role="menuitem"
            tabindex="-1"
            id="menu-item-0"
          >
            {{ object.Name }}
          </a>
        </div>
      </div>
    </div>








            <div class="relative inline-block text-left">
      <div>
        <button
          type="button"
          class="inline-flex justify-center w-full rounded-md border border-gray-300 shadow-sm px-4 py-2 bg-white text-sm font-medium text-gray-700 hover:bg-gray-50 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-offset-gray-100 focus:ring-indigo-500"
          id="menu-button"
          aria-expanded="true"
          aria-haspopup="true"
          @click="onUnitsDropDownClick"
        >
          Unit Data
          <!-- Heroicon name: solid/chevron-down -->
          <svg
            class="-mr-1 ml-2 h-5 w-5"
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 20 20"
            fill="currentColor"
            aria-hidden="true"
          >
            <path
              fill-rule="evenodd"
              d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
              clip-rule="evenodd"
            />
          </svg>
        </button>
      </div>

      <!--
    Dropdown menu, show/hide based on menu state.

    Entering: "transition ease-out duration-100"
      From: "transform opacity-0 scale-95"
      To: "transform opacity-100 scale-100"
    Leaving: "transition ease-in duration-75"
      From: "transform opacity-100 scale-100"
      To: "transform opacity-0 scale-95"
  -->
      <div
        class="scale-95 origin-top-right absolute right-0 mt-2 w-56 rounded-md shadow-lg bg-white ring-1 ring-black ring-opacity-5 focus:outline-none"
        v-bind:class="
          isUnitsDropdownOpen
            ? 'transform opacity-100 scale-100'
            : 'transform opacity-0 scale-95 hidden'
        "
        role="menu"
        aria-orientation="vertical"
        aria-labelledby="menu-button"
        tabindex="-1"
      >
        <div class="py-1" role="none">
          <!-- Active: "bg-gray-100 text-gray-900", Not Active: "text-gray-700" -->
          <a
            v-for="unit in unitsData"
            :key="unit.Id"
            @click="onUnitsItemClick"
            :data-units-item-name="unit.Name"
            class="text-gray-700 block px-4 py-2 text-sm"
            role="menuitem"
            tabindex="-1"
            id="menu-item-0"
          >
            {{ unit.Name }}
          </a>
        </div>
      </div>
    </div>













    <form class="w-full max-w-lg m-0 m-auto" v-if="selectedCraftsItem">
      <div class="flex flex-wrap flex-col -mx-3 mb-6">
        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            City Points
          </label>
          <input
            v-on:input="onChange"
            name="CityPoints"
            :value="selectedCraftsItem.CityPoints"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            City Price
          </label>
          <input
            v-on:input="onChange"
            name="CityPrice"
            :value="selectedCraftsItem.CityPrice"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Class
          </label>
          <input
            v-on:input="onChange"
            name="Class"
            :value="selectedCraftsItem.Class"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Crafting Text
          </label>
          <input
            v-on:input="onChange"
            name="Crafting Text"
            :value="selectedCraftsItem.CraftingText"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            HexColor
          </label>
          <input
            v-on:input="onChange"
            name="HexColor"
            :value="selectedCraftsItem.HexColor"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Id
          </label>
          <input
            v-on:input="onChange"
            name="Id"
            :value="selectedCraftsItem.Id"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Name
          </label>
          <input
            v-on:input="onChange"
            name="Name"
            :value="selectedCraftsItem.Name"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            OnDestroy
          </label>
          <input
            v-on:input="onChange"
            name="OnDestroy"
            :value="selectedCraftsItem.OnDestroy"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Proximity Bonus
          </label>
          <input
            v-on:input="onChange"
            name="Proximity Bonus"
            :value="selectedCraftsItem.ProximityBonus"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Proximity Penalty
          </label>
          <input
            v-on:input="onChange"
            name="Proximity Penalty"
            :value="selectedCraftsItem.ProximityPenalty"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Proximity Reverse
          </label>
          <input
            v-on:input="onChange"
            name="Proximity Reverse"
            :value="selectedCraftsItem.ProximityReverse"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Req1
          </label>
          <input
            v-on:input="onChange"
            name="Req1"
            :value="selectedCraftsItem.Req1"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Req2
          </label>
          <input
            v-on:input="onChange"
            name="Req2"
            :value="selectedCraftsItem.Req2"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Req3
          </label>
          <input
            v-on:input="onChange"
            name="Req3"
            :value="selectedCraftsItem.Req3"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Time0
          </label>
          <input
            v-on:input="onChange"
            name="Time0"
            :value="selectedCraftsItem.Time0"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Time1
          </label>
          <input
            v-on:input="onChange"
            name="Time1"
            :value="selectedCraftsItem.Time1"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Time2
          </label>
          <input
            v-on:input="onChange"
            name="Time2"
            :value="selectedCraftsItem.Time2"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Time3
          </label>
          <input
            v-on:input="onChange"
            name="Time3"
            :value="selectedCraftsItem.Time3"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Type
          </label>
          <input
            v-on:input="onChange"
            name="Type"
            :value="selectedCraftsItem.Type"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Value1
          </label>
          <input
            v-on:input="onChange"
            name="Value1"
            :value="selectedCraftsItem.Value1"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Value2
          </label>
          <input
            v-on:input="onChange"
            name="Value2"
            :value="selectedCraftsItem.Value2"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>

        <div class="w-full md:w-1/2 px-3">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-last-name"
          >
            Value3
          </label>
          <input
            v-on:input="onChange"
            name="Value3"
            :value="selectedCraftsItem.Value3"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-gray-200 rounded py-3 px-4 leading-tight focus:outline-none focus:bg-white focus:border-gray-500"
            id="grid-last-name"
            type="text"
            placeholder="Doe"
          />
        </div>
      </div>

      <button v-on:click="onCraftsSubmit">Submit</button>
    </form>


















<form class="w-full max-w-lg m-0 m-auto" v-if="selectedObjectsItem">

      <div class="flex flex-wrap flex-col -mx-3 mb-6">
        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            BlockChain ID
          </label>
          <input
            v-on:input="onObjectsChange"
            name="BlockChainID"
            :value="selectedObjectsItem.BlockChainID"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>


        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            BuildCost
          </label>
          <input
            v-on:input="onObjectsChange"
            name="BuildCost"
            :value="selectedObjectsItem.BuildCost"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            CanBuildUpon
          </label>
          <input
            v-on:input="onObjectsChange"
            name="CanBuildUpon"
            :value="selectedObjectsItem.CanBuildUpon"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>


        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            CanSelectCraft
          </label>
          <input
            v-on:input="onObjectsChange"
            name="CanSelectCraft"
            :value="selectedObjectsItem.CanSelectCraft"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            Capacity
          </label>
          <input
            v-on:input="onObjectsChange"
            name="Capacity"
            :value="selectedObjectsItem.Capacity"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            Class
          </label>
          <input
            v-on:input="onObjectsChange"
            name="Class"
            :value="selectedObjectsItem.Class"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>


        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            Construction
          </label>
          <input
            v-on:input="onObjectsChange"
            name="Construction"
            :value="selectedObjectsItem.Construction"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>



        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            CraftReqsMet
          </label>
          <input
            v-on:input="onObjectsChange"
            name="CraftReqsMet"
            :value="selectedObjectsItem.CraftReqsMet"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>



        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            CraftTimeMod
          </label>
          <input
            v-on:input="onObjectsChange"
            name="CraftTimeMod"
            :value="selectedObjectsItem.CraftTimeMod"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>



        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            Crafts
          </label>
          <input
            v-on:input="onObjectsChange"
            name="Crafts"
            :value="selectedObjectsItem.Crafts"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            Description
          </label>
          <input
            v-on:input="onObjectsChange"
            name="Description"
            :value="selectedObjectsItem.Description"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>


        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            DestroyCost
          </label>
          <input
            v-on:input="onObjectsChange"
            name="DestroyCost"
            :value="selectedObjectsItem.DestroyCost"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>


        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            Destroyable
          </label>
          <input
            v-on:input="onObjectsChange"
            name="Destroyable"
            :value="selectedObjectsItem.Destroyable"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            EdgeClass
          </label>
          <input
            v-on:input="onObjectsChange"
            name="EdgeClass"
            :value="selectedObjectsItem.EdgeClass"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            EdgeRequirements
          </label>
          <input
            v-on:input="onObjectsChange"
            name="EdgeRequirements"
            :value="selectedObjectsItem.EdgeRequirements"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            GoldCost
          </label>
          <input
            v-on:input="onObjectsChange"
            name="GoldCost"
            :value="selectedObjectsItem.GoldCost"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            HasDynamicGround
          </label>
          <input
            v-on:input="onObjectsChange"
            name="HasDynamicGround"
            :value="selectedObjectsItem.HasDynamicGround"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            Id
          </label>
          <input
            v-on:input="onObjectsChange"
            name="Id"
            :value="selectedObjectsItem.Id"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            InStore
          </label>
          <input
            v-on:input="onObjectsChange"
            name="InStore"
            :value="selectedObjectsItem.InStore"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>
        
        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            InputDeliver
          </label>
          <input
            v-on:input="onObjectsChange"
            name="InputDeliver"
            :value="selectedObjectsItem.InputDeliver"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            InputPickup
          </label>
          <input
            v-on:input="onObjectsChange"
            name="InputPickup"
            :value="selectedObjectsItem.InputPickup"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            LaborCost
          </label>
          <input
            v-on:input="onObjectsChange"
            name="LaborCost"
            :value="selectedObjectsItem.LaborCost"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            Name
          </label>
          <input
            v-on:input="onObjectsChange"
            name="Name"
            :value="selectedObjectsItem.Name"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            OutputDeliver
          </label>
          <input
            v-on:input="onObjectsChange"
            name="OutputDeliver"
            :value="selectedObjectsItem.OutputDeliver"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            OutputPickup
          </label>
          <input
            v-on:input="onObjectsChange"
            name="OutputPickup"
            :value="selectedObjectsItem.OutputPickup"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            PathBase
          </label>
          <input
            v-on:input="onObjectsChange"
            name="PathBase"
            :value="selectedObjectsItem.PathBase"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            PathMask
          </label>
          <input
            v-on:input="onObjectsChange"
            name="PathMask"
            :value="selectedObjectsItem.PathMask"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            PathMaskType
          </label>
          <input
            v-on:input="onObjectsChange"
            name="PathMaskType"
            :value="selectedObjectsItem.PathMaskType"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            ProximityDist
          </label>
          <input
            v-on:input="onObjectsChange"
            name="ProximityDist"
            :value="selectedObjectsItem.ProximityDist"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            ProximityEmit
          </label>
          <input
            v-on:input="onObjectsChange"
            name="ProximityEmit"
            :value="selectedObjectsItem.ProximityEmit"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            ProximityImmune
          </label>
          <input
            v-on:input="onObjectsChange"
            name="ProximityImmune"
            :value="selectedObjectsItem.ProximityImmune"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            QuestId
          </label>
          <input
            v-on:input="onObjectsChange"
            name="QuestId"
            :value="selectedObjectsItem.QuestId"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            Rotatable
          </label>
          <input
            v-on:input="onObjectsChange"
            name="Rotatable"
            :value="selectedObjectsItem.Rotatable"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            RotateTo
          </label>
          <input
            v-on:input="onObjectsChange"
            name="RotateTo"
            :value="selectedObjectsItem.RotateTo"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            StorageType
          </label>
          <input
            v-on:input="onObjectsChange"
            name="StorageType"
            :value="selectedObjectsItem.StorageType"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            TileWith
          </label>
          <input
            v-on:input="onObjectsChange"
            name="TileWith"
            :value="selectedObjectsItem.TileWith"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            UTValue
          </label>
          <input
            v-on:input="onObjectsChange"
            name="UTValue"
            :value="selectedObjectsItem.UTValue"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            UnitType
          </label>
          <input
            v-on:input="onObjectsChange"
            name="UnitType"
            :value="selectedObjectsItem.UnitType"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>



      </div>

      <button v-on:click="onObjectsSubmit">Submit</button>
    </form>










        <form class="w-full max-w-lg m-0 m-auto" v-if="selectedUnitsItem">
      <div class="flex flex-wrap flex-col -mx-3 mb-6">
        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            Area Mask
          </label>
          <input
            v-on:input="onUnitsChange"
            name="AreaMask"
            :value="selectedUnitsItem.AreaMask"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            Capacity
          </label>
          <input
            v-on:input="onUnitsChange"
            name="Capacity"
            :value="selectedUnitsItem.Capacity"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            Class
          </label>
          <input
            v-on:input="onUnitsChange"
            name="Class"
            :value="selectedUnitsItem.Class"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            Description2
          </label>
          <input
            v-on:input="onUnitsChange"
            name="Description2"
            :value="selectedUnitsItem.Description2"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            DescriptionClass
          </label>
          <input
            v-on:input="onUnitsChange"
            name="DescriptionClass"
            :value="selectedUnitsItem.DescriptionClass"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            GasReq
          </label>
          <input
            v-on:input="onUnitsChange"
            name="GasReq"
            :value="selectedUnitsItem.GasReq"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            HexColor
          </label>
          <input
            v-on:input="onUnitsChange"
            name="HexColor"
            :value="selectedUnitsItem.HexColor"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            Home
          </label>
          <input
            v-on:input="onUnitsChange"
            name="Home"
            :value="selectedUnitsItem.Home"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            Id
          </label>
          <input
            v-on:input="onUnitsChange"
            name="Id"
            :value="selectedUnitsItem.Id"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            Name
          </label>
          <input
            v-on:input="onUnitsChange"
            name="Name"
            :value="selectedUnitsItem.Name"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            NavType
          </label>
          <input
            v-on:input="onUnitsChange"
            name="NavType"
            :value="selectedUnitsItem.NavType"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>

        <div class="w-full md:w-1/2 px-3 mb-6 md:mb-0">
          <label
            class="block uppercase tracking-wide text-gray-700 text-xs font-bold mb-2"
            for="grid-first-name"
          >
            TravelSpeed
          </label>
          <input
            v-on:input="onUnitsChange"
            name="TravelSpeed"
            :value="selectedUnitsItem.TravelSpeed"
            class="appearance-none block w-full bg-gray-200 text-gray-700 border border-red-500 rounded py-3 px-4 mb-3 leading-tight focus:outline-none focus:bg-white"
            id="grid-first-name"
            type="text"
            placeholder="Jane"
          />
          <p class="text-red-500 text-xs italic">Please fill out this field.</p>
        </div>




      </div>

      <button v-on:click="onUnitsSubmit">Submit</button>
    </form>






  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "Crafts-Data",
  data() {
    return {

      craftsData: null,
      isCraftsDropdownOpen: false,
      selectedCraftsItem: null,

      objectsData: null,
      isObjectsDropdownOpen: false,
      selectedObjectsItem: null,

      unitsData: null,
      isUnitsDropdownOpen: false,
      selectedUnitsItem: null,

    };
  },
  watch: {
    craftsData: function (value) {
      console.log(value);
    },
    selectedCraftsItem: function (newValue) {
      console.log(newValue);
    },
  },
  methods: {
    onCraftsSubmit: function (e) {
      e.preventDefault();
      this.craftsData[this.selectedCraftsItem.Name] = this.selectedCraftsItem;
      axios
        .post("/api/crafting", this.craftsData)
        .then((response) => {
          console.log("response: ", response);
        })
        .catch((error) => {
          console.log("Error: ", error);
        });
    },
    onObjectsSubmit: function (e) {
      e.preventDefault();
      this.objectsData[this.selectedObjectsItem.Name] = this.selectedObjectsItem;
      axios
        .post("/api/objects", this.objectsData)
        .then((response) => {
          console.log("response: ", response);
        })
        .catch((error) => {
          console.log("Error: ", error);
        });
    },
    onUnitsSubmit: function (e) {
      e.preventDefault();
      this.unitsData[this.selectedUnitsItem.Name] = this.selectedUnitsItem;
      axios
        .post("/api/units", this.unitsData)
        .then((response) => {
          console.log("response: ", response);
        })
        .catch((error) => {
          console.log("Error: ", error);
        });
    },
    onChange: function (event) {
      this.selectedCraftsItem[event.target.name] = event.target.value;
      console.log(JSON.parse(JSON.stringify(this.selectedCraftsItem)));
    },
    onCraftsDropDownClick: function () {
      this.isCraftsDropdownOpen = !this.isCraftsDropdownOpen;
    },
    onCraftsItemClick: function (event) {
      // set selected item in data state
      this.selectedCraftsItem =
        this.craftsData[event.target.dataset.craftItemName];
        this.selectedObjectsItem = null;
this.selectedUnitsItem = null;
        this.isObjectsDropdownOpen = false;
        this.isUnitsDropdownOpen = false;
      // close dropdown
      this.isCraftsDropdownOpen = false;
    },
    onObjectsChange: function (event) {
      this.selectedObjectsItem[event.target.name] = event.target.value;
      console.log(JSON.parse(JSON.stringify(this.selectedObjectsItem)));
    },
    onObjectsDropDownClick: function () {
      console.log('onObjectsDropDownClick');
      this.isObjectsDropdownOpen = !this.isObjectsDropdownOpen;
    },
    onObjectsItemClick: function (event) {
      console.log('onObjectsItemClick: ', event.target.dataset);
      // set selected item in data state
      this.selectedObjectsItem =
        this.objectsData[event.target.dataset.objectsItemName];
        console.log('Selected objects item', this.selectedObjectsItem);

this.selectedCraftsItem = null;
this.selectedUnitsItem = null;

        this.isObjectsDropdownOpen = false;
        this.isUnitsDropdownOpen = false;
      // close dropdown
      this.isCraftsDropdownOpen = false;
    },
    onUnitsChange: function (event) {
      this.selectedUnitsItem[event.target.name] = event.target.value;
      console.log(JSON.parse(JSON.stringify(this.selectedUnitsItem)));
    },
    onUnitsDropDownClick: function () {
      console.log('onUnitsDropDownClick');
      this.isUnitsDropdownOpen = !this.isUnitsDropdownOpen;
    },
    onUnitsItemClick: function (event) {
      console.log('onUnitsItemClick: ', event.target.dataset);
      // set selected item in data state
      this.selectedUnitsItem =
        this.unitsData[event.target.dataset.unitsItemName];
        console.log('Selected units item', this.selectedunitsItem);

this.selectedCraftsItem = null;
this.selectedObjectsItem = null;

        this.isObjectsDropdownOpen = false;
        this.isCraftsDropdownOpen = false;
      // close dropdown
      this.isUnitsDropdownOpen = false;
    },
  },

  mounted() {
    axios
      .get("/api/crafting")
      .then((response) => {
        this.craftsData = response.data;
        console.log("response: ", response);
      })
      .catch((error) => {
        console.log("Error: ", error);
      });
    axios
      .get("/api/objects")
      .then((response) => {
        this.objectsData = response.data;
        console.log("response: ", response);
      })
      .catch((error) => {
        console.log("Error: ", error);
      });
    axios
      .get("/api/units")
      .then((response) => {
        this.unitsData = response.data;
        console.log("response: ", response);
      })
      .catch((error) => {
        console.log("Error: ", error);
      });
  },
  // logic
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
