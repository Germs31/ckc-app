<template>
  <v-row justify="center">
    <v-dialog v-model="dialog" persistent max-width="600px">
      <template v-slot:activator="{ on }">
        <v-btn color="primary" dark v-on="on">Open Dialog</v-btn>
      </template>
        <v-card>
            <v-card-title>
                <span class="headline">Add Book</span>
            </v-card-title>
            
            <v-card-text>
                <v-container>
                    <v-form>
                        <v-text-field label="Name of Book *" required></v-text-field>
                        <v-select v-model="category" :items="categories" label="Select A Category *"></v-select>
                        <v-text-field v-model="title" label="Enter Book Title *"></v-text-field>
                        <v-text-field v-model="author" label="Enter Book Author *"></v-text-field>
                        <v-textarea v-model="description" label="Enter Book Description *"></v-textarea>
                    </v-form>
                    
                </v-container>
                <small>*indicates required field</small>
            </v-card-text>

            <v-card-actions>
                <v-spacer></v-spacer>
                    <v-btn @click.stop="saveBook" color="green">Add</v-btn>
                    <v-btn color="green" text @click="dialog = false">Close</v-btn>
            </v-card-actions>
        </v-card>
    </v-dialog>
  </v-row>
</template>

<script>
    export default{
        data: () => ({
            dialog: false,
            catagory: "",
            title: "",
            author: "",
            description: "",
            categories: ["Recently read books", "Favorite books", "Best of the best"]
        }),

    }
</script>

